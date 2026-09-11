# 股票行情 — 1 个接口

> 本文件由 `tools/generate_catalog.py` 从 OpenAPI 规范自动生成，请勿手工编辑。

## us_stock_daily — 美国股票日行情

`GET /api/v1/data/us_stock_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 股票代码；操作符：in（逗号拆分多值（如 2024-01-01,2024-01-02））；默认值：AAPL | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 股票代码；默认返回 |
| `date` | string/date | 交易日期；默认返回 |
| `open` | number | 开盘价；默认返回 |
| `high` | number | 最高价；默认返回 |
| `low` | number | 最低价；默认返回 |
| `close` | number | 收盘价；默认返回 |
| `volume` | number | 成交量；默认返回 |
| `exchange_code` | string | 交易所编码；默认返回 |
| `country_code` | string | 国家编码；默认返回 |
| `currency_code` | string | 货币编码；默认返回 |
