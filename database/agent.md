## 說明 <!-- omit in toc -->

此為商品相關表格。

## 資料表快速連結<!-- omit in toc -->

- [data-agent|代理商申請表資料表](#data-agent%e4%bb%a3%e7%90%86%e5%95%86%e7%94%b3%e8%ab%8b%e8%a1%a8%e8%b3%87%e6%96%99%e8%a1%a8)
- [log-agent-apply|代理商申請資料表](#log-agent-apply%e4%bb%a3%e7%90%86%e5%95%86%e7%94%b3%e8%ab%8b%e8%b3%87%e6%96%99%e8%a1%a8)
- [log-agent-contract|代理商合約資料表](#log-agent-contract%e4%bb%a3%e7%90%86%e5%95%86%e5%90%88%e7%b4%84%e8%b3%87%e6%96%99%e8%a1%a8)

#### data-agent|代理商申請表資料表

資料表名稱: `data_agent`

中文名稱: 代理資料表

|     欄位     |     名稱     |                  設置                   | 說明                                         | 備註     |
| :----------: | :----------: | :-------------------------------------: | -------------------------------------------- | -------- |
|     `id`     |     編號     |    `int(20)`<br>`[null]`<br>`[pkey]`    | &nbsp;                                       | 自動編號 |
|    `name`    |     名稱     |  `varchar(64)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
|   `tax_id`   |   統一編號   | `varchar(16)`<br>`[null]`<br>`[unique]` | &nbsp;                                       | &nbsp;   |
|   `tel_no`   |   連絡電話   |  `varchar(32)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
|   `fax_no`   | 傳真電話(空) |  `varchar(32)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
|   `ramark`   |   備註(空)   |    `text(0)`<br>`[null]`<br>`[null]`    | &nbsp;                                       | &nbsp;   |
|   `status`   |     狀態     |  `tinyint(1)`<br>`[null]`<br>`[null]`   | `0`: 停用 <br> `1`: 啟用 <br>`2`: 合約簽署中 | &nbsp;   |
| `updated_by` | 更新人員(空) |  `varchar(128)`<br>`[null]`<br>`[idx]`  | &nbsp;                                       | &nbsp;   |
| `created_by` |   建立人員   |  `varchar(128)`<br>`[null]`<br>`[idx]`  | &nbsp;                                       | &nbsp;   |
|  `apply_at`  |   申請時間   |  `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                                       | &nbsp;   |
| `created_at` |   建立時間   |  `datetime(0)`<br>`[null]`<br>`[idx]`   | 申請通過時間                                 | &nbsp;   |
| `updated_at` |   更新時間   |  `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                                       | &nbsp;   |

#### log-agent-apply|代理商申請資料表

資料表名稱: `log_agent_apply`

中文名稱: 代理商申請資料表

|      欄位      |     名稱      |                  設置                   | 說明                                         | 備註     |
| :------------: | :-----------: | :-------------------------------------: | -------------------------------------------- | -------- |
|      `id`      |     編號      |    `int(20)`<br>`[null]`<br>`[pkey]`    | &nbsp;                                       | 自動編號 |
|     `name`     |     名稱      |  `varchar(64)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
|    `tax_id`    |   統一編號    | `varchar(16)`<br>`[null]`<br>`[unique]` | &nbsp;                                       | &nbsp;   |
|    `tel_no`    |   連絡電話    |  `varchar(32)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
|    `fax_no`    | 傳真電話(空)  |  `varchar(32)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
|    `ramark`    |   備註(空)    |    `text(0)`<br>`[null]`<br>`[null]`    | &nbsp;                                       | &nbsp;   |
| `image_link_1` | 上傳圖片1(空) | `varchar(255)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
| `image_link_2` | 上傳圖片2(空) | `varchar(255)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
| `image_link_3` | 上傳圖片3(空) | `varchar(255)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
| `image_link_4` | 上傳圖片4(空) | `varchar(255)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
| `image_link_5` | 上傳圖片5(空) | `varchar(255)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
| `image_link_6` | 上傳圖片6(空) | `varchar(255)`<br>`[null]`<br>`[null]`  | &nbsp;                                       | &nbsp;   |
|    `status`    |     狀態      |  `tinyint(1)`<br>`[null]`<br>`[null]`   | `0`: 失敗 <br> `1` :審核通過 <br>`2`: 審核中 | &nbsp;   |
|  `updated_by`  | 更新人員(空)  |  `varchar(128)`<br>`[null]`<br>`[idx]`  | &nbsp;                                       | &nbsp;   |
|  `updated_at`  |   更新時間    |  `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                                       | &nbsp;   |
|  `created_at`  |   建立時間    |  `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                                       | &nbsp;   |

#### log-agent-contract|代理商合約資料表

資料表名稱: `log_agent_contract`

中文名稱: 代理商合約資料表

|     欄位     |         名稱         |                 設置                  | 說明                                           | 備註     |
| :----------: | :------------------: | :-----------------------------------: | ---------------------------------------------- | -------- |
|     `id`     |         編號         |   `int(20)`<br>`[null]`<br>`[pkey]`   | &nbsp;                                         | 自動編號 |
|  `agent_id`  |      代理商編號      |   `int(20)`<br>`[null]`<br>`[null]`   | 可簽多筆合約                                   | &nbsp;   |
|    `name`    |         名稱         | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp; 合約名稱                                | &nbsp;   |
|  `content`   |       合約內容       |   `text(0)`<br>`[null]`<br>`[null]`   | 規劃是放合約的紙本或電子照片，符號隔開圖片連結 | &nbsp;   |
|  `is_back`   | 是否已經建立紙本存檔 | `tinyint(1)`<br>`[null]`<br>`[null]`  | &nbsp;                                         |
| `created_at` |       建立時間       | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                                         | &nbsp;   |
| `created_by` |       建立人員       | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                                         | &nbsp;   |
| `updated_at` |       更新時間       | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                                         | &nbsp;   |
| `updated_by` |     更新人員(空)     | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                                         | &nbsp;   |
