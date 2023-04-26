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

> Example of how to create an user:

```shell
curl --location 'https://example.com/erp_user/create' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email": "j.smith@test4.com",
    "password": "test",
    "name": "John Smith",
    "phone": "02323333",
    "language": "fr",
    "platform_type": 1,
    "shop_code": "jsmith",
    "shop_name": "John Smith Test Store",
    "website": "shop.apple.com",
    "address1": "1 Infinite Loop",
    "address2": "Suite 100",
    "city": "Cupertino",
    "state": "California",
    "zip": "95014",
    "country": "United States",
    "currency": "USD",
    "created_time": "2007-12-31T19:00:00-05:00",
    "updated_time": "2007-12-31T19:00:00-05:00",
    "timezone": "America/New_York",
    "latitude": 45.427408,
    "longitude": -75.68903,
    "multi_location_enabled": true,
    "cookie_consent_level": "implicit",
    "tags": ["enterprise"]
}'
```

```python
import requests
import json

url = "https://example.com/erp_user/create"

payload = json.dumps({
  "email": "j.smith@test4.com",
  "password": "test",
  "name": "John Smith",
  "phone": "02323333",
  "language": "fr",
  "platform_type": 1,
  "shop_code": "jsmith",
  "shop_name": "John Smith Test Store",
  "website": "shop.apple.com",
  "address1": "1 Infinite Loop",
  "address2": "Suite 100",
  "city": "Cupertino",
  "state": "California",
  "zip": "95014",
  "country": "United States",
  "currency": "USD",
  "created_time": "2007-12-31T19:00:00-05:00",
  "updated_time": "2007-12-31T19:00:00-05:00",
  "timezone": "America/New_York",
  "latitude": 45.427408,
  "longitude": -75.68903,
  "multi_location_enabled": True,
  "cookie_consent_level": "implicit",
  "tags": [
    "enterprise"
  ]
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)
```

```javascript
const axios = require('axios');
let data = JSON.stringify({
  "email": "example.com",
  "password": "example",
  "name": "example",
  "phone": "02323333",
  "language": "fr",
  "platform_type": 1,
  "shop_code": "jsmith",
  "shop_name": "John Smith Test Store",
  "website": "shop.apple.com",
  "address1": "1 Infinite Loop",
  "address2": "Suite 100",
  "city": "Cupertino",
  "state": "California",
  "zip": "95014",
  "country": "United States",
  "currency": "USD",
  "created_time": "2007-12-31T19:00:00-05:00",
  "updated_time": "2007-12-31T19:00:00-05:00",
  "timezone": "America/New_York",
  "latitude": 45.427408,
  "longitude": -75.68903,
  "multi_location_enabled": true,
  "cookie_consent_level": "implicit",
  "tags": [
    "enterprise"
  ]
});

let config = {
  method: 'post',
  maxBodyLength: Infinity,
  url: 'https://example.com/erp_user/create',
  headers: { 
    'Content-Type': 'application/json'
  },
  data : data
};

axios.request(config)
.then((response) => {
  console.log(JSON.stringify(response.data));
})
.catch((error) => {
  console.log(error);
});
```

This API is used to create an user.

### HTTP Request

`POST /erp_user/create`

### Request Body

This API requires user's info in the request body, which includes:

Data | Description
--------- | -----------
email |  
password |  
name |  
phone |  
language |
platform_type |
shop_code |
shop_name |
website |
address1 |
address2 |
city |
state |
zip |
country |
currency |
created_time |
updated_time |
timezone |
latitude |
longitude |
multi_location_enabled |
cookie_consent_level |
tags |

### Response

Please check the response example at right side.

> Successful response example:

```json
{
    "status": true,
    "msg": "User Created",
    "data": {
        "user_id": "120",
        "email": "example.com",
        "password": "test"
    }
}
```

## Create Website

> Example of how to create the website record:

```shell
curl --location 'https://api-stg.warp-driven.com/my_website/create' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email": "example.com",
    "password": "test",
    "website_code": "example_code",
    "platform_type": 1,
    "url": "example_website.com"
}'
```

```python
import requests
import json

url = "https://api-stg.warp-driven.com/my_website/create"

payload = json.dumps({
  "email": "example.com",
  "password": "test",
  "website_code": "exampel_code",
  "platform_type": 1,
  "url": "example_website.com"
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)
```

This API is used to create the website under the user account.

<aside class="notice">
Each user can create multiple websites.
</aside>



### HTTP Request

`POST /my_website/create`

### Request Body

Data | Description
--------- | -----------
email |  
password |  
website_code |  
platform_type |  
url |  

### Response

Please check the response example at right side.

> Successful response example:

```json
{
    "status": true,
    "msg": "ok",
    "data": {
        "website_code": "example_code",
        "user_id": "111",
        "platform_type": 1,
        "url": "example_website.com",
        "api_key": "meowmeowmeow",
        "create_dt": "2021-04-26T11:49:23Z"
    }
}
```

## Get Website API Key

> Example of how to :

```shell
curl --location 'https://example.com/my_website' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email": "example.com",
    "password": "test",
    "website_code": "example_website",
    "platform_type": 1
}'
```

```python
import requests
import json

url = "https://example.com/my_website"

payload = json.dumps({
  "email": "example.com",
  "password": "test",
  "website_code": "example_website",
  "platform_type": 1
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)
```

Each user can have multiple websites, and we will assign the unique API key for each website, and you can get the API key for the specific website via this API request. 

### HTTP Request

`POST /my_website`

### Request Body

Data | Description
--------- | -----------
email | 
password | 
website_code | 
platform_type | 

### Response

Please check the example at right side.

> Successful response example:

```json
{
    "status": true,
    "msg": "ok",
    "data": "meowmeowmeow"
}
```

## Get VSR Plan and Credit

> Example of how to get VSR(Visually Similar Recommendation) plan and credit:

```shell
curl --location 'https://example.com/ai_credit/plan?plan_id=1' \
--header 'X-API-Key: meowmeowmeow'
```

```python
import requests

url = "https://example.com/ai_credit/plan?plan_id=1"

payload = {}
headers = {
  'X-API-Key': 'meowmeowmeow'
}

response = requests.request("GET", url, headers=headers, data=payload)
```

This API is used to get the current plan detail for those plans you just subscribed when you [created the account](#erp-workflow).

`X-API-KEY: meowmeowmeow`

### HTTP Request

`GET /ai_credit/plan?plan_id=1`

### Request Parameters

Parameter | Description
--------- | -----------
[plan_id](#plan-id) | The plan type you have chosen when create the account.

<aside class="notice">
For authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

> Successful response example:

```json
{
    "status": true,
    "msg": "ok",
    "data": {
        "user_id": "2",
        "plan": {
            "plan_id": 1,
            "product_credit": 3996,
            "product_plan_credit": 4000,
            "plan_type": 1,
            "quota_renewal_date_left": 23,
            "quota_renewal_date": "2022-05-20T06:48:23Z",
            "plan_start_time": "2022-04-20T06:48:23Z",
            "plan_end_time": "2027-04-20T06:48:23Z"
        }
    }
}
```

## Get NLP Plan and Credit

> Example of how to get NLP plan and credit:

```shell
curl --location 'https://example.com/ai_credit/plan?plan_id=11' \
--header 'X-API-Key: meowmeowmeow'
```

```python
import requests

url = "https://example.com/ai_credit/plan?plan_id=11"

payload = {}
headers = {
  'X-API-Key': 'meowmeowmeow'
}

response = requests.request("GET", url, headers=headers, data=payload)
```

This API is used to get the current plan detail for those plans you just subscribed when you [created the account](#erp-workflow).

`X-API-KEY: meowmeowmeow`

### HTTP Request

`GET /ai_credit/plan?plan_id=11`

### Request Parameters

Parameter | Description
--------- | -----------
[plan_id](#plan-id) | The plan type you have chosen when create the account.

<aside class="notice">
For authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

> Successful response example:

```json
{
    "status": true,
    "msg": "ok",
    "data": {
        "user_id": "2",
        "plan": {
            "plan_id": 11,
            "product_credit": 1678,
            "product_plan_credit": 80000,
            "plan_type": 2,
            "quota_renewal_date_left": 23,
            "quota_renewal_date": "2023-05-20T07:11:16Z",
            "plan_start_time": "2023-04-20T07:11:16Z",
            "plan_end_time": "2023-05-20T07:11:16Z"
        }
    }
}
```