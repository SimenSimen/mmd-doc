## 說明 <!-- omit in toc -->

帳務相關表格。

## 資料表快速連結<!-- omit in toc -->


- [finance_bill|平台帳務資料表](#financebill%e5%b9%b3%e5%8f%b0%e5%b8%b3%e5%8b%99%e8%b3%87%e6%96%99%e8%a1%a8)
- [finance_bill_log|代理商繳款紀錄資料表](#financebilllog%e4%bb%a3%e7%90%86%e5%95%86%e7%b9%b3%e6%ac%be%e7%b4%80%e9%8c%84%e8%b3%87%e6%96%99%e8%a1%a8)


#### finance_bill|平台帳務資料表

資料表名稱: `finance_bill`

中文名稱: 平台帳務資料表

|     欄位     |     名稱     |                 設置                  | 說明                                                                          | 備註     |
| :----------: | :----------: | :-----------------------------------: | ----------------------------------------------------------------------------- | -------- |
|     `id`     |     編號     |   `int(10)`<br>`[null]`<br>`[pkey]`   | &nbsp;                                                                        | 自動編號 |
|  `agent_id`  |    代理id    |   `int(20)`<br>`[null]`<br>`[null]`   | &nbsp;                                                                        | &nbsp;   |
| `group_name` |   類別分組   | `varchar(32)`<br>`[null]`<br>`[null]` | 分組名稱                                                                      | &nbsp;   |
|   `amount`   |     金額     | `decimal(20,3)`<br>`[0]`<br>`[null]`  | 帳務金額                                                                      | &nbsp;   |
|  `currency`  |     幣別     | `varchar(32)`<br>`[null]`<br>`[null]` | &nbsp;                                                                        | &nbsp;   |
|   `remark`   |     備註     |    `text(0)`<br>`[0]`<br>`[null]`     | &nbsp;                                                                        | &nbsp;   |
|   `status`   |   處理狀態   |   `tinyint(1)`<br>`[0]`<br>`[null]`   | `0`: 未付款<br> `1`: 已結帳(收帳)<br> `2`: 取消<br> `3`: 未付清<br> `4`: 溢收 | &nbsp;   |
| `expired_by` | 過期時間(空) | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                                                                        | &nbsp;   |
| `created_at` |   建立時間   | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                                                                        | &nbsp;   |
| `create_by`  |   建立人員   | `varchar(32)`<br>`[null]`<br>`[null]` | &nbsp;                                                                        | &nbsp;   |
| `updated_at` | 更新時間(空) | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                                                                        | &nbsp;   |
| `updated_by` | 更新人員(空) | `varchar(32)`<br>`[null]`<br>`[null]` | &nbsp;                                                                        | &nbsp;   |

#### finance_bill_log|代理商繳款紀錄資料表

資料表名稱: `finance_bill_log`

中文名稱: 代理商繳款紀錄資料表

|     欄位     |   名稱   |                 設置                  | 說明     | 備註     |
| :----------: | :------: | :-----------------------------------: | -------- | -------- |
|     `id`     |   編號   |   `int(10)`<br>`[null]`<br>`[pkey]`   | &nbsp;   | 自動編號 |
|  `bill_id`   |  帳單id  |   `int(20)`<br>`[null]`<br>`[null]`   | &nbsp;   | &nbsp;   |
|    `type`    | 付款方式 | `varchar(16)`<br>`[null]`<br>`[null]` | &nbsp;   | &nbsp;   |
|   `amount`   |   金額   | `decimal(20,3)`<br>`[0]`<br>`[null]`  | 帳務金額 | &nbsp;   |
|   `remark`   |   備註   |    `text(0)`<br>`[0]`<br>`[null]`     | &nbsp;   | &nbsp;   |
| `created_at` | 建立時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;   | &nbsp;   |
