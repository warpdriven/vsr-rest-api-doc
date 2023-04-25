# Customer Managerment Service API

## Get User

> Example of how to :

```shell
curl --location 'https://example.com/erp_user?erp_user_email=example@example.com'
```

```python
import requests

url = "https://example.com/erp_user?erp_user_email=example@example.com"

payload = {}
headers = {}

response = requests.request("GET", url, headers=headers, data=payload)
```

```javascript
const axios = require('axios');

let config = {
  method: 'get',
  maxBodyLength: Infinity,
  url: 'https://example.com/erp_user?erp_user_email=example@example.com',
  headers: { }
};

axios.request(config)
.then((response) => {
  console.log(JSON.stringify(response.data));
})
.catch((error) => {
  console.log(error);
});
```

This API is used to check if the user existed or not. We are using the email of ERP user account to distinguish the unique user. To create an ERP account, please check [ERP Workflow](#erp-workflow).

### HTTP Request

`GET /erp_user?erp_user_email={user_email}`

### Request Parameters

Parameter | Description
--------- | -----------
erp_user_email | user account email

### Response

> Successful response example:

```json
{
    "status": true,
    "msg": "User Query",
    "data": false
}
```

## Create User

> Example of how to :

```shell
curl "http://example.com/api/kittens/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

```python
import os

print(f"This is an example")
```

Describe this API from here...

`X-API-KEY: meowmeowmeow`

### HTTP Request

`POST /product/delete/`

### Request Body

Data | Description
--------- | -----------
delete_shop_variant_ids | The list of [shop_variant_id](#product-property) 

<aside class="notice">
For authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

> Successful response example:

```json
```

## Create Website

> Example of how to :

```shell
curl "http://example.com/api/kittens/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

```python
import os

print(f"This is an example")
```

Describe this API from here...

`X-API-KEY: meowmeowmeow`

### HTTP Request

`POST /product/delete/`

### Request Body

Data | Description
--------- | -----------
delete_shop_variant_ids | The list of [shop_variant_id](#product-property) 

<aside class="notice">
For authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

> Successful response example:

```json
```

## Get Website API Key

> Example of how to :

```shell
curl "http://example.com/api/kittens/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

```python
import os

print(f"This is an example")
```

Describe this API from here...

`X-API-KEY: meowmeowmeow`

### HTTP Request

`POST /product/delete/`

### Request Body

Data | Description
--------- | -----------
delete_shop_variant_ids | The list of [shop_variant_id](#product-property) 

<aside class="notice">
For authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

> Successful response example:

```json
```

## Get VSR Plan and Credit

> Example of how to :

```shell
curl "http://example.com/api/kittens/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

```python
import os

print(f"This is an example")
```

Describe this API from here...

`X-API-KEY: meowmeowmeow`

### HTTP Request

`POST /product/delete/`

### Request Body

Data | Description
--------- | -----------
delete_shop_variant_ids | The list of [shop_variant_id](#product-property) 

<aside class="notice">
For authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

> Successful response example:

```json
```

## Get NLP Plan and Credit

> Example of how to :

```shell
curl "http://example.com/api/kittens/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

```python
import os

print(f"This is an example")
```

Describe this API from here...

`X-API-KEY: meowmeowmeow`

### HTTP Request

`POST /product/delete/`

### Request Body

Data | Description
--------- | -----------
delete_shop_variant_ids | The list of [shop_variant_id](#product-property) 

<aside class="notice">
For authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

> Successful response example:

```json
```