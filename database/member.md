## 說明<!-- omit in toc -->

會員資料相關表格

## 資料表快速連結<!-- omit in toc -->

- [data_member|會員基本資料表](#datamember%e6%9c%83%e5%93%a1%e5%9f%ba%e6%9c%ac%e8%b3%87%e6%96%99%e8%a1%a8)


#### data_member|會員基本資料表

資料表名稱: `data_member`

中文名稱: 會員基本資料表



|     欄位     |   名稱   |                   設置                   | 說明                               | 備註     |
| :----------: | :------: | :--------------------------------------: | ---------------------------------- | -------- |
|     `id`     |   編號   |    `int(10)`<br>`[null]`<br>`[pkey]`     | &nbsp;                             | 自動編號 |
|  `account`   |   帳號   | `varchar(128)`<br>`[null]`<br>`[unique]` | &nbsp;                             | &nbsp;   |
|  `password`  |   密碼   |  `varchar(128)`<br>`[null]`<br>`[null]`  | &nbsp;                             | &nbsp;   |
|    `name`    |   名稱   | `varchar(128)`<br>`[null]`<br>`[index]`  | &nbsp;                             | &nbsp;   |
|    `sex`     |   性別   |   `tinyint(1)`<br>`[null]`<br>`[null]`   | `0`: 未填 <br> `1`: 男<br> `2`: 女 | &nbsp;   |
|   `email`    |   信箱   | `varchar(128)`<br>`[null]`<br>`[unique]` | &nbsp;                             | &nbsp;   |
|  `phone_no`  | 行動電話 | `varchar(10)`<br>`[null]`<br>`[unique]`  | &nbsp;                             | &nbsp;   |
|   `tel_no`   |   市話   |  `varchar(64)`<br>`[null]`<br>`[null]`   | &nbsp;                             | &nbsp;   |
| `birthdate`  |   生日   |    `date(0)`<br>`[null]`<br>`[null]`     | 年月日                             | &nbsp;   |
| `group_name` | 分組名稱 |  `varchar(64)`<br>`[null]`<br>`[null]`   | 特定公司批發商、特約會員等類別     | &nbsp;   |
|   `active`   | 啟用狀態 |   `tinyint(1)`<br>`[null]`<br>`[null]`   | `0`: 停用 <br> `1`: 啟用           | &nbsp;   |
| `created_at` | 建立時間 |   `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                             | &nbsp;   |
| `updated_at` | 更新時間 |   `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                             | &nbsp;   |


