### API說明

### 規則

- API URL 將省略平台前綴進行書寫

### 文件配置

Api 文件須如下配置:

- 平台說明文件須填寫平台前綴字。
- 填寫 `URL` 如: `login`。
- 填寫 `Http Method` 如: `POST`。
- 填寫是否須登入，未填寫視為**須登入**。如: Auth: `N`。
- 請求參數須以json呈現，並在值的位置以註解說明。
- 若是選填的參數，則在索引**上方**加上`(option)`字樣。
- **回應**格式與**請求**相同。

### 商品列表(範例)

取得商品列表。

- URL: `items`
- Http Method: `GET`
- Auth: `Y`

**request**

```js
    {
        //option
        "classID": // 商品類別ID ,
    }
```

**response**

```js
    [
        {
            "menu_id": 1,
            "menu_name": "foo",
            //...
        },
        //...
    ]
```
----

### response 格式

- **正常**回傳值: 回傳`code 200`，**response body**本身即為資料。
- **錯誤操作/伺服器錯誤**: 回傳`code 500`。
- **找不到資源**: 回傳`code 404`。
- **沒有權限**: 回傳`code 403`。
- **錯誤**或**操作行為**之回傳格式如下

```js
    {
        "status": true, // error 為 false
        "message": "insert_success"
    }
```

