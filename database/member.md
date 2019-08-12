## 說明<!-- omit in toc -->

會員資料相關表格

## 資料表快速連結<!-- omit in toc -->

- [data_member|會員基本資料表](#datamember%E6%9C%83%E5%93%A1%E5%9F%BA%E6%9C%AC%E8%B3%87%E6%96%99%E8%A1%A8)


#### data_member|會員基本資料表

資料表名稱: `data_member`

中文名稱: 會員基本資料表



|     欄位     |    名稱    |                 設置                  | 說明                               | 備註     |
| :----------: | :--------: | :-----------------------------------: | ---------------------------------- | -------- |
|     `id`     |    編號    |   `int(10)`<br>`[null]`<br>`[pkey]`   | &nbsp;                             | 自動編號 |
|  `account`   |    帳號    | `varchar(128)`<br>`[null]`<br>`[unique]` | &nbsp;                             | &nbsp;   |
|  `password`  |    密碼    | `varchar(128)`<br>`[null]`<br>`[null]` | 區分橫幅區塊。                     | &nbsp;   |
|    `guid`    |   識別碼   | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                             | &nbsp;   |
|    `name`    |    名稱    | `varchar(128)`<br>`[null]`<br>`[null]` | &nbsp;                             | &nbsp;   |
|    `sex`     |    性別    | `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 未填 <br> `1`: 男<br> `1`: 女 | &nbsp;   |
|   `email`    |    信箱    | `varchar(128)`<br>`[null]`<br>`[null]` | &nbsp;                             | &nbsp;   |
|   `phone`    |  電話號碼  | `varchar(128)`<br>`[null]`<br>`[null]` | &nbsp;                             | &nbsp;   |
| `birthdate`  | 出生年月日 | `datetime(0)`<br>`[null]`<br>`[null]`  | &nbsp;                             | &nbsp;   |
|   `active`   |  啟用狀態  | `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 停用 <br> `1`: 啟用           | &nbsp;   |
| `created_at` |  建立時間  | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                             | &nbsp;   |
| `updated_at` |  更新時間  | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                             | &nbsp;   |
