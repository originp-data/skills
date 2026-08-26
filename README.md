# OPD 数据查询（opd-data）

通过 OPD 数据接口（`https://api.originp.com`）查询 A 股上市公司数据，覆盖 **62 个接口、6 大数据域**：基本信息、交易信息、财务信息、融资分配、重大事项、股权与治理。

本技能负责**获取数据**，返回结构化 JSON，可与 `echarts-ai-skill` 等图表技能配合完成可视化。

## 特性

- 零依赖：仅使用 Python 标准库（`urllib`），无需 `pip install`
- 通用查询：一个脚本覆盖全部 62 个接口，按需传参
- 字段可选：返回字段按接口文档自由指定，控制数据量
- 灵活过滤：支持多值（`in`）、区间（`between`）等过滤参数
- 分页拉取：`limit`/`offset` 控制返回行数，支持循环翻页取全量
- Key 安全管理：支持命令行、环境变量、配置文件三种方式，密钥本地保存

## 环境要求

- Python 3（含标准库）
- OPD API Key（形如 `opd_xxx`），由 OPD 平台分配

> **域名分工**：`https://data.originp.com/` 为注册/订阅等管理站点（提供页面）；`https://api.originp.com` 为接口调用地址，专供程序调用、不含页面。
>
> 注意：除 Key 外还需在 OPD 平台**订阅所需接口**（试用或购买套餐），未订阅的接口调用会返回 `BIZ_INTERFACE_FORBIDDEN`。

## 安装

将本技能目录复制到 OpenClaw 的技能目录（如 `~/.openclaw/workspace/skills/opd-data/`）即可。

## 配置 API Key（任选其一）

**方式一：命令行保存（推荐）**

```bash
python scripts/opd_query.py --set-key opd_你的Key
```

Key 保存到 `~/.opd/api_key`，立即生效，无需重启。若不想让 Key 出现在命令历史中，可运行 `python scripts/opd_query.py --set-key` 后按提示从标准输入粘贴。

**方式二：环境变量**

```bash
export OPD_API_KEY=opd_你的Key   # Linux/macOS
[Environment]::SetEnvironmentVariable("OPD_API_KEY", "opd_你的Key", "User")   # Windows
```

**验证配置：**

```bash
python scripts/opd_query.py --check
python scripts/opd_query.py co_info --fields sec_code --limit 1
```

返回 JSON 中 `code=0` 即成功。

## 快速开始

```bash
# 查询平安银行的证券简称与董事长
python scripts/opd_query.py co_info --fields sec_code,sec_name,chairman --sec_code 000001

# 查询 2024 年全年日行情收盘价
python scripts/opd_query.py daily_quote_hist --fields trade_date,close --sec_code 000001 --trade_date 2024-01-01,2024-12-31 --limit 300
```

## 调用方法

```
python scripts/opd_query.py <接口短名> --fields <字段1,字段2,...> [--过滤参数 值 ...] [--limit N] [--offset N]
```

### 常用参数

| 参数 | 说明 |
|---|---|
| `<接口短名>` | 接口标识，如 `co_info`、`daily_quote_hist`（也支持完整路径） |
| `--fields` | 必填。返回字段列表，逗号分隔，可选值见 `references/` 文档 |
| `--limit` | 单次返回行数，默认 20，最大 5000 |
| `--offset` | 分页位移，取全量时循环翻页直至返回为空 |
| `--过滤参数` | 任意接口过滤参数透传，多值逗号分隔（in）、区间逗号分隔两个边界（between） |
| `--api-key` | 临时指定 Key（优先级最高，覆盖环境变量与配置文件） |

### 响应格式

统一返回 `{code, message, data}`；业务错误同为 HTTP 200，`code != 0` 即失败。

## 数据域与接口

| 分类 | 参考文档 | 接口数 |
|---|---|---|
| 基本信息 | `references/catalog_basic.md` | 6 |
| 交易信息 | `references/catalog_trading.md` | 11 |
| 财务信息 | `references/catalog_finance.md` | 16 |
| 融资分配 | `references/catalog_financing.md` | 8 |
| 重大事项 | `references/catalog_events.md` | 6 |
| 股权与治理 | `references/catalog_governance.md` | 15 |

每个分类文档包含全部接口的**过滤参数说明**与**返回字段可选值**（标注"默认返回"的字段未指定时也会返回）。

## 错误码与处置

| 现象 | 原因 | 处置 |
|---|---|---|
| 提示"未配置 API Key" | Key 未配置 | 按上文配置 API Key |
| `code=20004`（API Key 无效） | Key 错误或已失效 | 重新获取 Key 并更新配置 |
| `BIZ_INTERFACE_FORBIDDEN` | 未订阅该接口 | 在 OPD 平台订阅该接口后重试 |
| `BIZ_PARAM_INVALID` | 参数错误 | 检查 `fields` 及过滤参数名/可选值 |
| 大量请求失败 | 超过每分钟 60 次限频 | 等待约 1 分钟，放慢节奏 |
| HTTP 5xx | 网络或服务端异常 | 稍后重试 |

## 图表可视化（可选增强）

本技能只负责取数。需要可视化时，可将查询得到的 `data` 数组整理为 `ChartRequest` JSON 交给 `echarts-ai-skill` 渲染（交互式 HTML）。例如 K 线图取 `daily_quote_hist` 的 `trade_date/open/close/low/high` 五个字段。

## 安全说明

- API Key 仅保存在 `~/.opd/api_key`（本地单用户受保护），不得写入其他文件
- Key 不会出现在查询请求的日志/命令历史中（`--set-key` 支持标准输入读取）

## 维护说明

`SKILL.md` 与 `references/` 文档由 OPD OpenAPI 规范自动生成，请勿手工编辑。
