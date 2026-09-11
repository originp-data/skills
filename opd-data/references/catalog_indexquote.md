# 指数行情 — 61 个接口

> 本文件由 `tools/generate_catalog.py` 从 OpenAPI 规范自动生成，请勿手工编辑。

## us_index_list — 美国指数清单

`GET /api/v1/data/us_index_list`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `index_name` | 否 | 指数名称；操作符：like（模糊匹配） | string |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `index_name` | string | 指数名称；默认返回 |

## us_index_daily — 美国指数日行情

`GET /api/v1/data/us_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：BANK | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## us_index_weekly — 美国指数周行情

`GET /api/v1/data/us_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：BANK | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## us_index_monthly — 美国指数月行情

`GET /api/v1/data/us_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：BANK | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## us_index_yearly — 美国指数年行情

`GET /api/v1/data/us_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：BANK | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## hk_index_daily — 中国香港指数日行情

`GET /api/v1/data/hk_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：HSCEI | string | HSCEI - 国企指数；HSI - 恒生指数；HSTECH - 恒生科技指数；VHSI - 恒生波幅指数 |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## hk_index_weekly — 中国香港指数周行情

`GET /api/v1/data/hk_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：HSCEI | string | HSCEI - 国企指数；HSI - 恒生指数；HSTECH - 恒生科技指数；VHSI - 恒生波幅指数 |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## hk_index_monthly — 中国香港指数月行情

`GET /api/v1/data/hk_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：HSCEI | string | HSCEI - 国企指数；HSI - 恒生指数；HSTECH - 恒生科技指数；VHSI - 恒生波幅指数 |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## hk_index_yearly — 中国香港指数年行情

`GET /api/v1/data/hk_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：HSCEI | string | HSCEI - 国企指数；HSI - 恒生指数；HSTECH - 恒生科技指数；VHSI - 恒生波幅指数 |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## jp_index_daily — 日本指数日行情

`GET /api/v1/data/jp_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：JNIV | string | JNIV - NikkeiVolatility；JPXNK400 - JPX-Nikkei400；MTHR - TopixMotherMarket；MTHRDV - MothersGeneralTR；N225 - Nikkei225；N300 - Nikkei300；SPTPX - S&P/TOPIX150；TOPX - TOPIX；TOPXDV - TopixDV；TX500 - TOPIX500；XDN - JapaneseYenCurrencyIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## jp_index_weekly — 日本指数周行情

`GET /api/v1/data/jp_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：JNIV | string | JNIV - NikkeiVolatility；JPXNK400 - JPX-Nikkei400；MTHR - TopixMotherMarket；MTHRDV - MothersGeneralTR；N225 - Nikkei225；N300 - Nikkei300；SPTPX - S&P/TOPIX150；TOPX - TOPIX；TOPXDV - TopixDV；TX500 - TOPIX500；XDN - JapaneseYenCurrencyIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## jp_index_monthly — 日本指数月行情

`GET /api/v1/data/jp_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：JNIV | string | JNIV - NikkeiVolatility；JPXNK400 - JPX-Nikkei400；MTHR - TopixMotherMarket；MTHRDV - MothersGeneralTR；N225 - Nikkei225；N300 - Nikkei300；SPTPX - S&P/TOPIX150；TOPX - TOPIX；TOPXDV - TopixDV；TX500 - TOPIX500；XDN - JapaneseYenCurrencyIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## jp_index_yearly — 日本指数年行情

`GET /api/v1/data/jp_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：JNIV | string | JNIV - NikkeiVolatility；JPXNK400 - JPX-Nikkei400；MTHR - TopixMotherMarket；MTHRDV - MothersGeneralTR；N225 - Nikkei225；N300 - Nikkei300；SPTPX - S&P/TOPIX150；TOPX - TOPIX；TOPXDV - TopixDV；TX500 - TOPIX500；XDN - JapaneseYenCurrencyIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## tw_index_daily — 中国台湾指数日行情

`GET /api/v1/data/tw_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：TWII | string | TWII - Taiwan Weighted |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## tw_index_weekly — 中国台湾指数周行情

`GET /api/v1/data/tw_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：TWII | string | TWII - Taiwan Weighted |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## tw_index_monthly — 中国台湾指数月行情

`GET /api/v1/data/tw_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：TWII | string | TWII - Taiwan Weighted |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## tw_index_yearly — 中国台湾指数年行情

`GET /api/v1/data/tw_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：TWII | string | TWII - Taiwan Weighted |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## kr_index_daily — 韩国指数日行情

`GET /api/v1/data/kr_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：KOSDAQ | string | KOSDAQ - KosdaqCompositeIndex；KOSPI200 - KOSPI200；KQ11 - KosdaqCompositeIndex；KS11 - KOSPI；KS200 - KOSPI200 |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## kr_index_weekly — 韩国指数周行情

`GET /api/v1/data/kr_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：KOSDAQ | string | KOSDAQ - KosdaqCompositeIndex；KOSPI200 - KOSPI200；KQ11 - KosdaqCompositeIndex；KS11 - KOSPI；KS200 - KOSPI200 |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## kr_index_monthly — 韩国指数月行情

`GET /api/v1/data/kr_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：KOSDAQ | string | KOSDAQ - KosdaqCompositeIndex；KOSPI200 - KOSPI200；KQ11 - KosdaqCompositeIndex；KS11 - KOSPI；KS200 - KOSPI200 |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## kr_index_yearly — 韩国指数年行情

`GET /api/v1/data/kr_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：KOSDAQ | string | KOSDAQ - KosdaqCompositeIndex；KOSPI200 - KOSPI200；KQ11 - KosdaqCompositeIndex；KS11 - KOSPI；KS200 - KOSPI200 |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## de_index_daily — 德国指数日行情

`GET /api/v1/data/de_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：0O7N | string | 0O7N - ScaleAllShareGREUR；BIXR - BETTERINVESTING100INDEX；BIXX - BTRINVSTNG100INDEX；CDAXX - CDAX(Performance)Index；DE30 - DowJonesGermanyTitans30Index；DE30D - DowJonesGermanyTitans30USD；DE30DT - DowJonesGermanyTitans30TotalReturnUS；DE30TR - DJGermany30TR；GDAXHI - HDAXPerformance；GDAXHIP - HDAXPrice；GDAXI - DAXIndex；GDAXIP - DAXPrice；GDAXP - DAXKursindex；MDAXI - DAXMidcap；MKDX - DAXMidcapPrice；SDAXI - SDAXIndex(SDXP)；TECDAX - TecDAX；V1X - VDAX-NEW/DAXNewVolatility |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## de_index_weekly — 德国指数周行情

`GET /api/v1/data/de_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：0O7N | string | 0O7N - ScaleAllShareGREUR；BIXR - BETTERINVESTING100INDEX；BIXX - BTRINVSTNG100INDEX；CDAXX - CDAX(Performance)Index；DE30 - DowJonesGermanyTitans30Index；DE30D - DowJonesGermanyTitans30USD；DE30DT - DowJonesGermanyTitans30TotalReturnUS；DE30TR - DJGermany30TR；GDAXHI - HDAXPerformance；GDAXHIP - HDAXPrice；GDAXI - DAXIndex；GDAXIP - DAXPrice；GDAXP - DAXKursindex；MDAXI - DAXMidcap；MKDX - DAXMidcapPrice；SDAXI - SDAXIndex(SDXP)；TECDAX - TecDAX；V1X - VDAX-NEW/DAXNewVolatility |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## de_index_monthly — 德国指数月行情

`GET /api/v1/data/de_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：0O7N | string | 0O7N - ScaleAllShareGREUR；BIXR - BETTERINVESTING100INDEX；BIXX - BTRINVSTNG100INDEX；CDAXX - CDAX(Performance)Index；DE30 - DowJonesGermanyTitans30Index；DE30D - DowJonesGermanyTitans30USD；DE30DT - DowJonesGermanyTitans30TotalReturnUS；DE30TR - DJGermany30TR；GDAXHI - HDAXPerformance；GDAXHIP - HDAXPrice；GDAXI - DAXIndex；GDAXIP - DAXPrice；GDAXP - DAXKursindex；MDAXI - DAXMidcap；MKDX - DAXMidcapPrice；SDAXI - SDAXIndex(SDXP)；TECDAX - TecDAX；V1X - VDAX-NEW/DAXNewVolatility |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## de_index_yearly — 德国指数年行情

`GET /api/v1/data/de_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：0O7N | string | 0O7N - ScaleAllShareGREUR；BIXR - BETTERINVESTING100INDEX；BIXX - BTRINVSTNG100INDEX；CDAXX - CDAX(Performance)Index；DE30 - DowJonesGermanyTitans30Index；DE30D - DowJonesGermanyTitans30USD；DE30DT - DowJonesGermanyTitans30TotalReturnUS；DE30TR - DJGermany30TR；GDAXHI - HDAXPerformance；GDAXHIP - HDAXPrice；GDAXI - DAXIndex；GDAXIP - DAXPrice；GDAXP - DAXKursindex；MDAXI - DAXMidcap；MKDX - DAXMidcapPrice；SDAXI - SDAXIndex(SDXP)；TECDAX - TecDAX；V1X - VDAX-NEW/DAXNewVolatility |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## gb_index_list — 英国指数清单

`GET /api/v1/data/gb_index_list`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `index_name` | 否 | 指数名称；操作符：like（模糊匹配） | string |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `index_name` | string | 指数名称；默认返回 |

## gb_index_daily — 英国指数日行情

`GET /api/v1/data/gb_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：AIM1 | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## gb_index_weekly — 英国指数周行情

`GET /api/v1/data/gb_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：AIM1 | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## gb_index_monthly — 英国指数月行情

`GET /api/v1/data/gb_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：AIM1 | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## gb_index_yearly — 英国指数年行情

`GET /api/v1/data/gb_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：AIM1 | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## fr_index_list — 法国指数清单

`GET /api/v1/data/fr_index_list`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `index_name` | 否 | 指数名称；操作符：like（模糊匹配） | string |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `index_name` | string | 指数名称；默认返回 |

## fr_index_daily — 法国指数日行情

`GET /api/v1/data/fr_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：CACEG | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## fr_index_weekly — 法国指数周行情

`GET /api/v1/data/fr_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：CACEG | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## fr_index_monthly — 法国指数月行情

`GET /api/v1/data/fr_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：CACEG | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## fr_index_yearly — 法国指数年行情

`GET /api/v1/data/fr_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：CACEG | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## in_index_list — 印度指数清单

`GET /api/v1/data/in_index_list`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `index_name` | 否 | 指数名称；操作符：like（模糊匹配） | string |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `index_name` | string | 指数名称；默认返回 |

## in_index_daily — 印度指数日行情

`GET /api/v1/data/in_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：BSE100 | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## in_index_weekly — 印度指数周行情

`GET /api/v1/data/in_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：BSE100 | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## in_index_monthly — 印度指数月行情

`GET /api/v1/data/in_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：BSE100 | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## in_index_yearly — 印度指数年行情

`GET /api/v1/data/in_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：BSE100 | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## au_index_list — 澳大利亚指数清单

`GET /api/v1/data/au_index_list`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `index_name` | 否 | 指数名称；操作符：like（模糊匹配） | string |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `index_name` | string | 指数名称；默认返回 |

## au_index_daily — 澳大利亚指数日行情

`GET /api/v1/data/au_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：AFLI | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## au_index_weekly — 澳大利亚指数周行情

`GET /api/v1/data/au_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：AFLI | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## au_index_monthly — 澳大利亚指数月行情

`GET /api/v1/data/au_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：AFLI | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## au_index_yearly — 澳大利亚指数年行情

`GET /api/v1/data/au_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；默认值：AFLI | string |  |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## id_index_daily — 印尼指数日行情

`GET /api/v1/data/id_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：IDX30 | string | IDX30 - IDX30Jakarta；JKLQ45 - IDXLQ45；JKSE - JakartaStockExchangeCompositeIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## id_index_weekly — 印尼指数周行情

`GET /api/v1/data/id_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：IDX30 | string | IDX30 - IDX30Jakarta；JKLQ45 - IDXLQ45；JKSE - JakartaStockExchangeCompositeIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## id_index_monthly — 印尼指数月行情

`GET /api/v1/data/id_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：IDX30 | string | IDX30 - IDX30Jakarta；JKLQ45 - IDXLQ45；JKSE - JakartaStockExchangeCompositeIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## id_index_yearly — 印尼指数年行情

`GET /api/v1/data/id_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：IDX30 | string | IDX30 - IDX30Jakarta；JKLQ45 - IDXLQ45；JKSE - JakartaStockExchangeCompositeIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## th_index_daily — 泰国指数日行情

`GET /api/v1/data/th_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：SET | string | SET - StockExchangeofThailandSETIndex；SET100 - SET100Index；SET50 - SET50Index；SETTRI - SETTotalReturnIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## th_index_weekly — 泰国指数周行情

`GET /api/v1/data/th_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：SET | string | SET - StockExchangeofThailandSETIndex；SET100 - SET100Index；SET50 - SET50Index；SETTRI - SETTotalReturnIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## th_index_monthly — 泰国指数月行情

`GET /api/v1/data/th_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：SET | string | SET - StockExchangeofThailandSETIndex；SET100 - SET100Index；SET50 - SET50Index；SETTRI - SETTotalReturnIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## th_index_yearly — 泰国指数年行情

`GET /api/v1/data/th_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：SET | string | SET - StockExchangeofThailandSETIndex；SET100 - SET100Index；SET50 - SET50Index；SETTRI - SETTotalReturnIndex |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## my_index_daily — 马来西亚指数日行情

`GET /api/v1/data/my_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：BMCON | string | BMCON - BursaMalaysiaConstructionIndex；BMPLA - BursaMalaysiaPlantationIndex；BMTEC - BursaMalaysiaTechnologyIndex；KLSE - FTSEBursaMalaysiaKLCI；KLTE - KLTechnology(BursaMalaysia) |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## my_index_weekly — 马来西亚指数周行情

`GET /api/v1/data/my_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：BMCON | string | BMCON - BursaMalaysiaConstructionIndex；BMPLA - BursaMalaysiaPlantationIndex；BMTEC - BursaMalaysiaTechnologyIndex；KLSE - FTSEBursaMalaysiaKLCI；KLTE - KLTechnology(BursaMalaysia) |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## my_index_monthly — 马来西亚指数月行情

`GET /api/v1/data/my_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：BMCON | string | BMCON - BursaMalaysiaConstructionIndex；BMPLA - BursaMalaysiaPlantationIndex；BMTEC - BursaMalaysiaTechnologyIndex；KLSE - FTSEBursaMalaysiaKLCI；KLTE - KLTechnology(BursaMalaysia) |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## my_index_yearly — 马来西亚指数年行情

`GET /api/v1/data/my_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：BMCON | string | BMCON - BursaMalaysiaConstructionIndex；BMPLA - BursaMalaysiaPlantationIndex；BMTEC - BursaMalaysiaTechnologyIndex；KLSE - FTSEBursaMalaysiaKLCI；KLTE - KLTechnology(BursaMalaysia) |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## ca_index_daily — 加拿大指数日行情

`GET /api/v1/data/ca_index_daily`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：GSPTSE | string | GSPTSE - S&PTSXCompositeIndex(Canada)；GSPTXDV - S&P/TSXDividendAristocrats；SPTSX60 - S&P/TSX60INDEX；TRGSPTSE - S&P/TSXCompositeTotalReturn；TRGSPTSEU - S&P/TSXCompositeTRUSD；TRX50CAP - ThomsonReutersCanada50；TTCD - TSXConsumerDiscretionaryCappedIndex；TTCS - TSXConsumerStaplesCappedIndex；TTEN - TSXEnergyCappedIndex；TTFS - TSXFinancialsCappedIndex；TTHC - TSXHealthCareCappedIndex；TTIN - TSXIndustrialsCappedIndex；TTMT - TSXMaterialsCappedIndex；TTRE - TSXRealEstateCappedIndex；TTTK - TSXInformationTechCappedIndex；TTTS - TSXTelecomServicesCappedIndex；TTUT - TSXUtilitiesCappedIndex；TXBA - S&P/TSXCompositeIndex-Banks；TXBE - S&P/TSXEqualWeightGlobalBas |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## ca_index_weekly — 加拿大指数周行情

`GET /api/v1/data/ca_index_weekly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：GSPTSE | string | GSPTSE - S&PTSXCompositeIndex(Canada)；GSPTXDV - S&P/TSXDividendAristocrats；SPTSX60 - S&P/TSX60INDEX；TRGSPTSE - S&P/TSXCompositeTotalReturn；TRGSPTSEU - S&P/TSXCompositeTRUSD；TRX50CAP - ThomsonReutersCanada50；TTCD - TSXConsumerDiscretionaryCappedIndex；TTCS - TSXConsumerStaplesCappedIndex；TTEN - TSXEnergyCappedIndex；TTFS - TSXFinancialsCappedIndex；TTHC - TSXHealthCareCappedIndex；TTIN - TSXIndustrialsCappedIndex；TTMT - TSXMaterialsCappedIndex；TTRE - TSXRealEstateCappedIndex；TTTK - TSXInformationTechCappedIndex；TTTS - TSXTelecomServicesCappedIndex；TTUT - TSXUtilitiesCappedIndex；TXBA - S&P/TSXCompositeIndex-Banks；TXBE - S&P/TSXEqualWeightGlobalBas |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## ca_index_monthly — 加拿大指数月行情

`GET /api/v1/data/ca_index_monthly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：GSPTSE | string | GSPTSE - S&PTSXCompositeIndex(Canada)；GSPTXDV - S&P/TSXDividendAristocrats；SPTSX60 - S&P/TSX60INDEX；TRGSPTSE - S&P/TSXCompositeTotalReturn；TRGSPTSEU - S&P/TSXCompositeTRUSD；TRX50CAP - ThomsonReutersCanada50；TTCD - TSXConsumerDiscretionaryCappedIndex；TTCS - TSXConsumerStaplesCappedIndex；TTEN - TSXEnergyCappedIndex；TTFS - TSXFinancialsCappedIndex；TTHC - TSXHealthCareCappedIndex；TTIN - TSXIndustrialsCappedIndex；TTMT - TSXMaterialsCappedIndex；TTRE - TSXRealEstateCappedIndex；TTTK - TSXInformationTechCappedIndex；TTTS - TSXTelecomServicesCappedIndex；TTUT - TSXUtilitiesCappedIndex；TXBA - S&P/TSXCompositeIndex-Banks；TXBE - S&P/TSXEqualWeightGlobalBas |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |

## ca_index_yearly — 加拿大指数年行情

`GET /api/v1/data/ca_index_yearly`

> **调用说明**：版本：1.0；调用限频：每分钟 60 次；单次最大记录数：1000
> **鉴权**：请求头 `X-API-Key: opd_xxx`；需已订阅该接口，否则返回 BIZ_INTERFACE_FORBIDDEN。

**过滤参数**（`fields` 必填、`limit`/`offset` 分页为统一参数，见 SKILL.md）

| 参数 | 必填 | 说明 | 类型 | 示例 / 可选值 |
|---|---|---|---|---|
| `ticker` | 是 | 指数名称；枚举值按「value - label」展示（value 为实际传参值，label 为含义），调用时仅传 value 部分；默认值：GSPTSE | string | GSPTSE - S&PTSXCompositeIndex(Canada)；GSPTXDV - S&P/TSXDividendAristocrats；SPTSX60 - S&P/TSX60INDEX；TRGSPTSE - S&P/TSXCompositeTotalReturn；TRGSPTSEU - S&P/TSXCompositeTRUSD；TRX50CAP - ThomsonReutersCanada50；TTCD - TSXConsumerDiscretionaryCappedIndex；TTCS - TSXConsumerStaplesCappedIndex；TTEN - TSXEnergyCappedIndex；TTFS - TSXFinancialsCappedIndex；TTHC - TSXHealthCareCappedIndex；TTIN - TSXIndustrialsCappedIndex；TTMT - TSXMaterialsCappedIndex；TTRE - TSXRealEstateCappedIndex；TTTK - TSXInformationTechCappedIndex；TTTS - TSXTelecomServicesCappedIndex；TTUT - TSXUtilitiesCappedIndex；TXBA - S&P/TSXCompositeIndex-Banks；TXBE - S&P/TSXEqualWeightGlobalBas |
| `date` | 否 | 交易日期；操作符：between（逗号分隔两个边界） | string/date-time |  |

**返回字段**（`fields` 参数可选值；标注"默认返回"的字段在未指定时也会返回）

| 字段 | 类型 | 说明 |
|---|---|---|
| `ticker` | string | 指数代码；默认返回 |
| `date` | string/date-time | 交易日期；默认返回 |
| `open` | number | 开盘；默认返回 |
| `high` | number | 最高；默认返回 |
| `low` | number | 最低；默认返回 |
| `close` | number | 收盘；默认返回 |
| `volume` | number | 成交量；默认返回 |
