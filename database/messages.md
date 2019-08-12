## 說明 <!-- omit in toc -->

此為訊息相關表格。

## 資料表快速連結<!-- omit in toc -->

- [u-chat-room|留言板資料表](#u-chat-room%e7%95%99%e8%a8%80%e6%9d%bf%e8%b3%87%e6%96%99%e8%a1%a8)
- [u-chat|聊天訊息資料表](#u-chat%e8%81%8a%e5%a4%a9%e8%a8%8a%e6%81%af%e8%b3%87%e6%96%99%e8%a1%a8)
- [u-inbox|信箱收件夾資料表](#u-inbox%e4%bf%a1%e7%ae%b1%e6%94%b6%e4%bb%b6%e5%a4%be%e8%b3%87%e6%96%99%e8%a1%a8)
- [u-mail|信件資料表](#u-mail%e4%bf%a1%e4%bb%b6%e8%b3%87%e6%96%99%e8%a1%a8)

#### u-chat-room|留言板資料表

資料表名稱: `u_chat_room`

中文名稱: 留言板(聊天室)資料表

|     欄位     |      名稱      |                  設置                  | 說明                                       | 備註     |
| :----------: | :------------: | :------------------------------------: | ------------------------------------------ | -------- |
|     `id`     |      編號      |   `int(20)`<br>`[null]`<br>`[pkey]`    | &nbsp;                                     | 自動編號 |
| `group_name` |    群組名稱    |  `varchar(64)`<br>`[null]`<br>`[idx]`  | 分類用                                     | &nbsp;   |
|  `user_key`  | 使用者索引(空) | `varchar(255)`<br>`[null]`<br>`[null]` | 聊天室所屬人員或平台, 空值為系統使用       | &nbsp;   |
|   `status`   |      狀態      |  `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 停用 <br> `1`: 啟用                   | &nbsp;   |
| `updated_by` |    更新時間    |  `datetime(0)`<br>`[null]`<br>`[idx]`  | 聊天室更新時間，對話紀錄更新時也會一併更新 | &nbsp;   |
| `created_by` |    建立人員    | `varchar(128)`<br>`[null]`<br>`[idx]`  | &nbsp;                                     | &nbsp;   |
| `created_at` |    建立時間    |  `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                                     | &nbsp;   |

#### u-chat|聊天訊息資料表

資料表名稱: `u_chat`

中文名稱: 聊天訊息資料表

|      欄位      |    名稱    |                  設置                  | 說明                              | 備註     |
| :------------: | :--------: | :------------------------------------: | --------------------------------- | -------- |
|      `id`      |    編號    |   `int(20)`<br>`[null]`<br>`[pkey]`    | &nbsp;                            | 自動編號 |
|   `room_id`    |  聊天室id  |   `int(20)`<br>`[null]`<br>`[null]`    | &nbsp;                            | &nbsp;   |
|    `title`     |  標題(空)  | `varchar(255)`<br>`[null]`<br>`[idx]`  | &nbsp;                            | &nbsp;   |
|   `content`    |    內容    |   `text(0)`<br>`[null]`<br>`[null]`    | &nbsp;                            | &nbsp;   |
|    `status`    |    狀態    |  `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 屏蔽 <br> `1`: 正常          | &nbsp;   |
|  `user_type`   | 使用者類別 |  `tinyint(1)`<br>`[null]`<br>`[null]`  | 使用者類別                        | &nbsp;   |
|   `user_key`   | 使用者索引 | `varchar(255)`<br>`[null]`<br>`[null]` | 使用者唯一id , 可找出該使用者憑據 | &nbsp;   |
|      `ip`      |   發送IP   |  `varchar(32)`<br>`[null]`<br>`[idx]`  | 紀錄IP                            | &nbsp;   |
| `client_agent` |  用戶平台  | `varchar(128)`<br>`[null]`<br>`[null]` | 紀錄客戶端                        | &nbsp;   |
|    `device`    |   發送IP   | `varchar(16)`<br>`[null]`<br>`[null]`  | 紀錄裝置                          | &nbsp;   |
|  `updated_by`  |  更新時間  |  `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                            | &nbsp;   |
|  `created_at`  |  建立時間  |  `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                            | &nbsp;   |

FK1: `room_id` reference `u_chat_room(id)` cascade update,delete

#### u-inbox|信箱收件夾資料表

資料表名稱: `u_inbox`

中文名稱: 信箱收件夾資料表

|      欄位      |    名稱    |                    設置                    | 說明                              | 備註     |
| :------------: | :--------: | :----------------------------------------: | --------------------------------- | -------- |
|      `id`      |    編號    |     `int(20)`<br>`[null]`<br>`[pkey]`      | &nbsp;                            | 自動編號 |
| `amount_limit` |  限制數量  |    `tinyint(5)`<br>`[150]`<br>`[null]`     | 限制一個收件夾的信件上限          | &nbsp;   |
|  `user_type`   | 使用者類別 |  `tinyint(1)`<br>`[null]`<br>`[unique_1]`  | 使用者類別                        | &nbsp;   |
|   `user_key`   | 使用者索引 | `varchar(255)`<br>`[null]`<br>`[unique_1]` | 使用者唯一id , 可找出該使用者憑據 | &nbsp;   |

#### u-mail|信件資料表

資料表名稱: `u_mail`

中文名稱: 信件資料表

|      欄位      |    名稱    |                  設置                  | 說明                                            | 備註     |
| :------------: | :--------: | :------------------------------------: | ----------------------------------------------- | -------- |
|      `id`      |    編號    |   `int(20)`<br>`[null]`<br>`[pkey]`    | &nbsp;                                          | 自動編號 |
|   `inbox_id`   |   信箱id   |   `int(20)`<br>`[null]`<br>`[null]`    | 信箱id                                          | &nbsp;   |
|     `type`     |    種類    |   `tinyint(1)`<br>`[1]`<br>`[null]`    | 1: 正常信件 <br>2: 寄件備份信件 <br>3: 草稿     | &nbsp;   |
|    `title`     |    標題    | `varchar(255)`<br>`[null]`<br>`[idx]`  | &nbsp;                                          | &nbsp;   |
|  `sub_title`   |   副標題   | `varchar(255)`<br>`[null]`<br>`[idx]`  | &nbsp;                                          | &nbsp;   |
|   `content`    |    內容    |    `text(0)`<br>`[null]`<br>`[idx]`    | &nbsp;                                          | &nbsp;   |
|   `is_open`    | 是否開啟過 |  `tinyint(1)`<br>`[null]`<br>`[null]`  | 紀錄是否點開來看過                              | &nbsp;   |
|      `ip`      |   發送IP   |  `varchar(32)`<br>`[null]`<br>`[idx]`  | 紀錄IP                                          | &nbsp;   |
| `client_agent` |  用戶平台  | `varchar(128)`<br>`[null]`<br>`[null]` | 紀錄客戶端                                      | &nbsp;   |
|    `device`    |   發送IP   | `varchar(16)`<br>`[null]`<br>`[null]`  | 紀錄裝置                                        | &nbsp;   |
|  `source_id`   |  信件來源  |   `int(20)`<br>`[null]`<br>`[null]`    | 紀錄信件來源信箱id                              | &nbsp;   |
|  `user_type`   | 使用者類別 |  `tinyint(1)`<br>`[null]`<br>`[null]`  | 使用者類別                                      | &nbsp;   |
|   `user_key`   | 使用者索引 | `varchar(255)`<br>`[null]`<br>`[null]` | 使用者唯一id , 可找出該使用者憑據，紀錄送出人員 | &nbsp;   |
|  `created_at`  |  建立時間  |  `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                                          | &nbsp;   |