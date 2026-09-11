# 产业链数据 — 3 个接口

> 本文件由 `tools/generate_catalog.py` 从 OpenAPI 规范自动生成，请勿手工编辑。

## chain_list — 产业链清单

`GET /api/v1/data/chain_list`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `chain_name` | 否 | 产业链名称；操作符：like（模糊匹配） | string | `半导体%` |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `chain_name` | string | 产业链名称；默认返回 |
| `introduction` | string | 产业介绍 |
| `participant_info` | string | 产业参与企业情况介绍 |

## chain_graph — 产业链图谱

`GET /api/v1/data/chain_graph`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `chain_name` | 是 | 产业链名称；默认值：半导体产业链 | string |  |
| `chain_stage` | 否 | 产业环节 | string | 上游；中游；下游 |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `chain_name` | string | 产业链名称；默认返回 |
| `chain_stage` | string | 产业环节；默认返回 |
| `product_category` | string | 产品分类；默认返回 |
| `product_name` | string | 产品名称；默认返回 |
| `related_company` | string | 关联公司；默认返回 |

## product_relation — 产品关联公司

`GET /api/v1/data/product_relation`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `sec_code` | 是 | 股票代码；操作符：in（逗号拆分多值（如 2024-01-01,2024-01-02）） | string |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `company_name` | string | 公司名称；默认返回 |
| `sec_code` | string | 股票代码；默认返回 |
| `product_name` | string | 具体产品；默认返回 |
