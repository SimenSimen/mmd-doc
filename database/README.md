# 資料庫設計

## 開發說明

資料庫設計協作開發須有**明確規範**，因此下列規定須遵守。

### 命名規則

-   需要前綴字以區分資料庫用途，如: data_item
-   複合字以 \_ 符號分隔開，如: admin_menu, parent_no
-   避免使用資料庫關鍵字，如:

**case, asc, desc, where, select, from, table, alter, or, and, between, order**
... 等等。

-   資料表盡量以單數命名，若框架產生之資料表則無須再修改
-   統一欄位名稱如下表：

|        欄位        |    名稱    | 說明                                         | 備註   |
| :----------------: | :--------: | -------------------------------------------- | ------ |
|        `id`        |    編號    | primay key 流水號                            | &nbsp; |
| `parent_{column}`  |  關聯欄位  | 需填上欄位名稱                               | &nbsp; |
| `{table}_{column}` |  關聯欄位  | 需填上資料表名稱以及關聯欄位，前綴字不須填入 | &nbsp; |
|       `name`       |    名稱    | &nbsp;                                       | &nbsp; |
|      `email`       |   E-mail   | &nbsp;                                       | &nbsp; |
|     `account`      |    帳號    | &nbsp;                                       | &nbsp; |
|     `password`     |    密碼    | &nbsp;                                       | &nbsp; |
|       `type`       |    類別    | &nbsp;                                       | &nbsp; |
|   `{name}_type`    | (名稱)類別 | &nbsp;                                       | &nbsp; |
|     `phone_no`     |  行動電話  | &nbsp;                                       | &nbsp; |
|      `tel_no`      |    市話    | &nbsp;                                       | &nbsp; |
|    `group_name`    |  分組名稱  | 分組、區塊使用                               | &nbsp; |
|   `description`    |    描述    | &nbsp;                                       | &nbsp; |
|     `content`      |    內容    | &nbsp;                                       | &nbsp; |
|      `title`       |    標題    | &nbsp;                                       | &nbsp; |
|      `remark`      |    備註    | &nbsp;                                       | &nbsp; |
|    `sub_title`     |   副標題   | &nbsp;                                       | &nbsp; |
|      `status`      |    狀態    | &nbsp;                                       | &nbsp; |
|   `is\_{status}`   |    開關    | 需填上狀態，如 `is_opening`                  | &nbsp; |
|     `sort_no`      |  排列序號  | &nbsp;                                       | &nbsp; |
|    `created_at`    |  建立時間  | &nbsp;                                       | &nbsp; |
|    `updated_at`    |  更新時間  | &nbsp;                                       | &nbsp; |
|    `created_by`    |  建立人員  | &nbsp;                                       | &nbsp; |
|    `updated_by`    |  更新人員  | &nbsp;                                       | &nbsp; |
| `{operation}\_at`  |  時間紀錄  | 需填上執行動作，如 `delete_at`               | &nbsp; |

-   若有用途同上統一欄位名稱的欄位需求，則以前綴字分別`{name}_{column}`，如: 第二組密碼，`second_password`。

### 前綴字

前綴字的用途在於為資料表分類，方便在查找或是須要大量搜尋的時候使用。

| 前綴字  |   名稱   | 說明                                                       | 備註   |
| :-----: | :------: | ---------------------------------------------------------- | ------ |
| `_data` | 營運資料 | 通常為使用者輸入產生，如商品、新聞等等，並且是可被搜尋的。 | &nbsp; |
|  `_u`   | 工具資料 | 通常為元件之資料表，如網站設定、橫幅、Menu等等             | &nbsp; |
| `_log`  | 紀錄資料 | 通常為系統產生紀錄之資料表                                 | &nbsp; |

## 文件說明

### 資料表格式說明

-   鍵值填寫: 主建為 `pkey_{name}`, 普通索引為 `idx_{name}`, 唯一索引 `unique_{name}`，只有一個欄位的時候 `{name}` 可不填。
-   欄位設置說明: <br>`data type(data length)`<br>`[default value]`<br>`[index name]`，若無值則填null。
-   空值: 若可空值，則書寫至中文名稱後方，如 `名稱(空)`
-   說明盡量書寫完整

