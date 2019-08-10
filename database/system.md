## 說明

此為系統相關表格。

-   [操作紀錄表(log_action)](#操作紀錄表log_action)

### 操作紀錄表(log_action)

|     欄位     |   名稱   |                  設置                  | 說明                           | 備註     |
| :----------: | :------: | :------------------------------------: | ------------------------------ | -------- |
|     `id`     |   編號   |   `int(20)`<br>`[null]`<br>`[pkey]`    | &nbsp;                         | 自動編號 |
|    `name`    |   名稱   | `varchart(64)`<br>`[null]`<br>`[null]` | 英文命名                       | &nbsp;   |
| `user_type`  |  使用者  |  `tinyint(1)`<br>`[null]`<br>`[null]`  | 自行定義使用者                 | &nbsp;   |
| `group_name` | 群組名稱 | `varchart(64)`<br>`[null]`<br>`[idx]`  | 英文命名，用來分組紀錄         | &nbsp;   |
|   `ramark`   | 備註(空) | `text(0)`<br>`[null]`<br>`[null],yes`  | &nbsp;                         | &nbsp;   |
|   `status`   |   狀態   |  `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 失敗 <br> `1`: 成功       | &nbsp;   |
| `created_by` | 建立人員 | `varchart(128)`<br>`[null]`<br>`[idx]` | 根據使用者名稱填寫，不關聯原表 | &nbsp;   |
| `created_at` | 建立時間 |  `datetime(0)`<br>`[null]`<br>`[idx]`  | 英文命名，用來分組紀錄         | &nbsp;   |

