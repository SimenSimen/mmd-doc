## 說明 <!-- omit in toc -->
此為系統相關表格。

## 資料表快速連結<!-- omit in toc -->

- [log-action|操作紀錄表](#log-action%e6%93%8d%e4%bd%9c%e7%b4%80%e9%8c%84%e8%a1%a8)

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

