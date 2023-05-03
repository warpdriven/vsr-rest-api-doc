# Visual Search API

Once you have subscribed to the Visual Search plan, and you have enough credits, you should be able to use our VS API to get similar products to get recommendations.

To get the visual search results, You should always init your products via [Nuwa Upsert API](#insert-products) first, and make sure the task id status and process are successful by [VS credit and status API](#get-vs-credit-and-status).

## Search API

> Example of how to make a visual search API:

```shell
curl --location --request POST 'http://example.com/vs/internal_search?shop_variant_id=001' \
--header 'X-API-Key: meowmeowmeow'
```

```python
url = "http://example.com/vs/internal_search?shop_variant_id=001"

payload = {}
headers = {
  'X-API-Key': 'meowmeowmeow'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)
```

```javascript
const axios = require('axios');

let config = {
  method: 'post',
  maxBodyLength: Infinity,
  url: 'http://example.com/vs/internal_search?shop_variant_id=001',
  headers: { 
    'X-API-Key': 'meowmeowmeow'
  }
};

axios.request(config)
.then((response) => {
  console.log(JSON.stringify(response.data));
})
.catch((error) => {
  console.log(error);
});
```

In this API, you will need to provide the target product's shop_variant_id, and the API will return all visual similar products for you. The return results are sorted by similar score rank of DESC.

`X-API-KEY: meowmeowmeow`

### HTTP Request

`POST /internal_search?shop_variant_id={id}`

### Request Parameters

Parameter | Description
--------- | -----------
[shop_variant_id](#product-property) | The unique id for each product. 

<aside class="notice">
If you just init your products by Nuwa API, you probably will not get the visual search results immediately, because training AI model and calculating vectors for images are time-consuming jobs. You should check the status and progress via the task id and make sure it has been succesful.
</aside>

### Response

The max num of similar visual search results are 20 products. You will find the, score and recall strategy for each candidate product.

> Successful response example:

```json
[
    {
        "shop_variant_id": "001",
        "score": 2.0,
        "recall_type": "2"
    },
    {
        "shop_variant_id": "002",
        "score": 1.5857766,
        "recall_type": "2"
    },
    ...
]
```

## Get VS Credit and Status 

> Example of how to make a visual search API:

```shell
curl --location 'https://example.com/latest/vs/get_vs_credit_status?plan_id=1' \
--header 'X-API-Key: meowmeowmeow'
```

```python
import requests

url = "https://example.com/latest/vs/get_vs_credit_status?plan_id=1"

payload = {}
headers = {
  'X-API-Key': 'meowmeowmeow'
}

response = requests.request("GET", url, headers=headers, data=payload)

print(response.text)
```

```javascript
const axios = require('axios');

let config = {
  method: 'get',
  maxBodyLength: Infinity,
  url: 'https://example.com/latest/vs/get_vs_credit_status?plan_id=1',
  headers: { 
    'X-API-Key': 'meowmeowmeow'
  }
};

axios.request(config)
.then((response) => {
  console.log(JSON.stringify(response.data));
})
.catch((error) => {
  console.log(error);
});

```

Describe this API from here...

`X-API-KEY: meowmeowmeow`

### HTTP Request

`GET /get_vs_credit_status?plan_id=1`

### Request Parameters

Parameter | Description
--------- | -----------
[plan_id](#plan-id) | The ID of VS service. 

<aside class="notice">
For authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

If you don't have any running task, the response will only bring back the credit info. Otherwise, you should also get the **task_progress** and **task_status**.

> Successful response example:

```json
{
    "status": true,
    "msg": "ok",
    "data": {
        "plan_id": 1,
        "product_credit": 3594,
        "product_plan_credit": 4000,
        "plan_type": 1,
        "quota_renewal_date_left": 16,
        "quota_renewal_date": "2023-05-20T06:48:23Z",
        "plan_start_time": "2023-04-20T06:48:23Z",
        "plan_end_time": "2027-04-20T06:48:23Z",
        "is_expired": false,
        "task_progress": 100,
        "task_status": "SUCCESS"
    }
}

or 

{
    "status": true,
    "msg": "ok",
    "data": {
        "plan_id": 1,
        "product_credit": 3594,
        "product_plan_credit": 4000,
        "plan_type": 1,
        "quota_renewal_date_left": 16,
        "quota_renewal_date": "2023-05-20T06:48:23Z",
        "plan_start_time": "2023-04-20T06:48:23Z",
        "plan_end_time": "2027-04-20T06:48:23Z",
        "is_expired": false
    }
}
```