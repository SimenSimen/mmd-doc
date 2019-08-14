## 說明 <!-- omit in toc -->
此為系統相關表格。

## 資料表快速連結<!-- omit in toc -->

- [log-action|操作紀錄表](#log-action%e6%93%8d%e4%bd%9c%e7%b4%80%e9%8c%84%e8%a1%a8)
- [u_web_config|網站設定表](#uwebconfig%e7%b6%b2%e7%ab%99%e8%a8%ad%e5%ae%9a%e8%a1%a8)

#### log-action|操作紀錄表

資料表名稱: `log_action`

中文名稱: 操作紀錄表

|     欄位     |   名稱   |                 設置                  | 說明                     | 備註     |
| :----------: | :------: | :-----------------------------------: | ------------------------ | -------- |
|     `id`     |   編號   |   `int(20)`<br>`[null]`<br>`[pkey]`   | &nbsp;                   | 自動編號 |
|    `name`    |   名稱   | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
| `user_type`  |  使用者  | `tinyint(1)`<br>`[null]`<br>`[null]`  | 自行定義使用者           | &nbsp;   |
| `group_name` | 群組名稱 | `varchar(64)`<br>`[null]`<br>`[idx]`  | 分組紀錄                 | &nbsp;   |
|   `ramark`   | 備註(空) |   `text(0)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|   `status`   |   狀態   | `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 失敗 <br> `1`: 成功 | &nbsp;   |
| `created_by` | 建立人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | 填入使用者的KEY          | &nbsp;   |
| `created_at` | 建立時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |

#### u_web_config|網站設定表

資料表名稱: `u_web_config`

中文名稱: 網站設定表

**(待新增欄位)** 等待確切功能，目前只有資訊。

|       欄位        |      名稱      |                  設置                  | 說明                     | 備註     |
| :---------------: | :------------: | :------------------------------------: | ------------------------ | -------- |
|       `id`        |      編號      |   `int(20)`<br>`[null]`<br>`[pkey]`    | &nbsp;                   | 自動編號 |
|      `name`       |    網站名稱    | `varchar(255)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
|  `company_name`   |    公司名稱    | `varchar(255)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
|      `email`      |  公司信箱(空)  | `varchar(255)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
| `company_address` |  公司地址(空)  | `varchar(255)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
| `company_manager` | 公司負責人(空) | `varchar(255)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
|    `phone_no`     |  手機號碼(空)  | `varchar(32)`<br>`[null]`<br>`[null]`  | &nbsp;                   | &nbsp;   |
|   `phone_no_2`    | 手機號碼2(空)  | `varchar(32)`<br>`[null]`<br>`[null]`  | &nbsp;                   | &nbsp;   |
|     `tel_no`      |  市話號碼(空)  | `varchar(32)`<br>`[null]`<br>`[null]`  | &nbsp;                   | &nbsp;   |
|    `tel_no_2`     | 市話號碼2(空)  | `varchar(32)`<br>`[null]`<br>`[null]`  | &nbsp;                   | &nbsp;   |
|    `tel_no_3`     | 市話號碼3(空)  | `varchar(32)`<br>`[null]`<br>`[null]`  | &nbsp;                   | &nbsp;   |
|     `fax_no`      |  傳真號碼(空)  | `varchar(32)`<br>`[null]`<br>`[null]`  | &nbsp;                   | &nbsp;   |
| `unavailable_msg` |  網站維護訊息  | `varchar(64)`<br>`[null]`<br>`[null]`  | &nbsp;                   | &nbsp;   |
|    `one_limit`    |    一筆限制    |  `tinyint(1)`<br>`[1]`<br>`[unique ]`  | 限制config只有一筆資料   | &nbsp;   |
|     `status`      |      狀態      |  `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 關閉 <br> `1`: 啟用 | &nbsp;   |
|  `main_currency`  |    主要幣別    |  `varchar(32)`<br>`[TWD]`<br>`[null]`  | 主要收款幣別             | &nbsp;   |
|   `created_by`    |    建立人員    | `varchar(128)`<br>`[null]`<br>`[idx]`  | 填入使用者的KEY          | &nbsp;   |
|   `created_at`    |    建立時間    |  `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |

