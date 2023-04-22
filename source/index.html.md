---
title: API Reference

language_tabs: # must be one of https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers
  - shell
  - python
  - javascript
  - php

toc_footers:
  - <a href='https://warp-driven.com/'>Documentation Powered by Warp Driven</a>
  - <a href='https://warp-driven.com/'>Abourt Us</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the Kittn API
---

# Introduction

Welcome to the [Warp Driven](https://warp-driven.com/) API Document! You can use our API to access Warp Driven API endpoints, which can integrate Warp Driven services to sysytems of clients.

Our API provides a way for E-commerce websites to interact with our recommendation system and AI capabilities, in order to enhance their customers' online-shopping experience.

Our API is designed to be flexible and scalable, allowing e-commerce clients to easily integrate our services into their existing systems. With our API, clients can access our powerful AI technology, which is able to analyze customer behavior and provide personalized recommendations, resulting in increased sales and customer satisfaction.

This document will provide a comprehensive guide to our API, including instructions on how to access and use our various endpoints. We will also provide information on the parameters required for each endpoint, as well as example requests and responses.

Whether you are a developer looking to integrate our services into your e-commerce website, or a business owner looking to improve your online shopping experience, our API documentation will provide you with all the information you need to get started.

You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Example

## Delete API example

```shell
curl "http://example.com/api/kittens/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

```python
import os

print(f"This is an example")
```

> JSON response example:

```json
{
  "id": 000,
  "deleted" : ":("
}
```

> Make sure to use Warp Driven assigned `X-API-KEY`.

This is an example API for document.
For **Authorization** in API header, please add the ==X-API-KEY== API key, which is assigned by Warp Driven.

`X-API-KEY: abcabc`

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
test_param_1 | false | Test is test.
test_param_2 | true | Test is test 2.

<aside class="success">
You must replace <code>abcabc</code> with your personal API key.
</aside>

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

<aside class="warning">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Nuwa API

## Product Property

Our API allows you to manage the product. We define a standard product object, which includes crucial and basic properties to describe the product.

> Example of a product object:

```json
{
    "shop_variant_id": "001",
    "shop_product_id": "shop_product_id-001",
    "sku": "sku-001",
    "product_id": "product_id-001",
    "barcode": "my-barcode",
    "is_default_variant": true,
    "title": "my-title",
    "stock_quantity": 100,
    "stock_status": 1,
    "description": "Description text is here",
    "categories": [
        {
            "cat_id": 1,
            "cat_name": "Clothing"
        }
    ],
    "brand": "my-brand",
    "main_image_url": "https://test/image/link",
    "image_urls": [
        "www.image1.com",
        "www.image2.com"
    ],
    "product_link": "https://example.com/product/link/",
    "type": "variable",
    "status": 1,
    "regular_price": 100.00,
    "price": 99.00,
    "sale_price": 50.00,
    "cost_price": 0,
    "weight": 118.5,
    "colour": "green",
    "size": "large",
    "on_sale": false,
    "purchasable": false,
    "related_ids": [
        31
    ],
    "meta_fields": [
        {
            "key": "country",
            "value": "AUS",
            "type": ""
        }
    ],
    "date_created_gmt": "2017-03-23T20:03:12",
    "date_modified_gmt": "2017-03-23T20:03:12"
}
```

### Product Property Description

Attribute | Data Type | Nullable | Description
--------- | --------- | -------- |  -----------
shop_variant_id | String | **No** | The unique id for product
shop_product_id | String | **No** | 
sku             | String | Yes | 
product_id | String | Yes | 
barcode | String | Yes | 
is_default_variant | Bool | Yes | 
title | String | **No** | 
stock_quantity | String | Yes | 
stock_status | Integer | Yes | 
description | String | Yes | 
short_description | String | Yes | 
categories | [Category](#category-property) List | Yes | 
brand | String | Yes | 
main_image_url | String | Yes | 
image_urls | String List | Yes | 
product_link | String | Yes | 
type | String | Yes | 
status | Interger | Yes | 
regular_price | Float | Yes | 
price | Float | Yes | 
sale_price | Float | Yes | 
cost_price | Float | Yes | 
price_currency | String | Yes | 
on_sale | Bool | Yes | 
purchasable | Bool | Yes | 
related_ids | Interger List | Yes | 
weight | Float | Yes | 
colour | String | Yes | 
size | String | Yes |
meta_fields | [Metadata](#metadata-property) List | Yes | 
date_created_gmt | Date | Yes |  
date_modified_gmt | Date | Yes |   

<aside class="success">
Remember — To have a successful response, you cannot add the attibute which is not included in the above table.
</aside>

## Category Property

The categories attribute consists of a list of category objects. You can add multiple category objects in the list to descript your product.

> Example of a categories attibute:

```json
"categories": [
                {
                    "cat_id": 1,
                    "cat_name": "Clothing"
                },
                {
                    "cat_id": 100,
                    "cat_name": "Sofa"
                }
            ]
```

### Category Property Description

Attribute | Data Type | Nullable | Description
--------- | --------- | -------- |  -----------
cat_id | String | **No** | The id of category
cat_name | String | **No** | The name of category

<aside class="success">
Remember — To add a category object, you should only contain <code>cat_id</code> and <code>cat_name</code> in it.
</aside>

## Metadata Property

The meta_fields attribute consists of a list of metadata object. You can add multiple metadata objects in the list to provide any kind of extra data for the product.

> Example of a categories attibute:

```json
"meta_fields": [
                {
                    "key": "country",
                    "value": "AUS",
                    "type": ""
                },
                {
                    "key": "delivery",
                    "value": "ship",
                    "type": ""
                }
            ]
```

### Category Property Description

Attribute | Data Type | Nullable | Description
--------- | --------- | -------- |  -----------
key | String | **No** | The name of this metadata
value | String | **No** | The name of this metadata
type | String | **No** | It is flexible to fulfill any info

<aside class="success">
Remember — To add a metadata object, you should only contain <code>key</code>, <code>value</code> and <code>type</code> in it.
</aside>

## Insert Products

> Example of how to insert new products:

```shell
curl --location 'https://example.com/product/upsert/' \
--header 'Content-Type: application/json' \
--header 'X-API-Key: meowmeowmeow' \
--data '{
    "items": [
        {
            "shop_variant_id": "001",
            "shop_product_id": "shop_product_id-001",
            "sku": "sku-001",
            "product_id": "product_id-001",
            "barcode": "my-barcode",
            "is_default_variant": true,
            "title": "my-title",
            "stock_quantity": 100,
            "stock_status": 1,
            "description": "Description text is here",
            "categories": [
                {
                    "cat_id": 1,
                    "cat_name": "Clothing"
                }
            ],
            "brand": "my-brand",
            "main_image_url": "https://test/image/link",
            "image_urls": [
                "www.image1.com",
                "www.image2.com"
            ],
            "product_link": "https://example.com/product/link/",
            "type": "variable",
            "status": 1,
            "regular_price": 100.00,
            "price": 99.00,
            "sale_price": 50.00,
            "cost_price": 0,
            "weight": 118.5,
            "colour": "green",
            "size": "large",
            "on_sale": false,
            "purchasable": false,
            "related_ids": [
                31
            ],
            "meta_fields": [
                {
                    "key": "country",
                    "value": "AUS",
                    "type": ""
                }
            ],
            "date_created_gmt": "2017-03-23T20:03:12",
            "date_modified_gmt": "2017-03-23T20:03:12"
        }
    ]
}'
```

```python
import requests
import json

url = "https://example.com/product/upsert/"

payload = json.dumps({
  "items": [
    {
          "shop_variant_id": "001",
          "shop_product_id": "shop_product_id-001",
          "sku": "sku-001",
          "product_id": "product_id-001",
          "barcode": "my-barcode",
          "is_default_variant": true,
          "title": "my-title",
          "stock_quantity": 100,
          "stock_status": 1,
          "description": "Description text is here",
          "categories": [
              {
                  "cat_id": 1,
                  "cat_name": "Clothing"
              }
          ],
          "brand": "my-brand",
          "main_image_url": "https://test/image/link",
          "image_urls": [
              "www.image1.com",
              "www.image2.com"
          ],
          "product_link": "https://example.com/product/link/",
          "type": "variable",
          "status": 1,
          "regular_price": 100.00,
          "price": 99.00,
          "sale_price": 50.00,
          "cost_price": 0,
          "weight": 118.5,
          "colour": "green",
          "size": "large",
          "on_sale": false,
          "purchasable": false,
          "related_ids": [
              31
          ],
          "meta_fields": [
              {
                  "key": "country",
                  "value": "AUS",
                  "type": ""
              }
          ],
          "date_created_gmt": "2017-03-23T20:03:12",
          "date_modified_gmt": "2017-03-23T20:03:12"
      }
  ]
})

headers = {
  'Content-Type': 'application/json',
  'X-API-Key': 'meowmeowmeow'
}

response = requests.request("POST", url, headers=headers, data=payload)
```

```javascript
const axios = require('axios');
let data = JSON.stringify({
  "items": [
    {
          "shop_variant_id": "001",
          "shop_product_id": "shop_product_id-001",
          "sku": "sku-001",
          "product_id": "product_id-001",
          "barcode": "my-barcode",
          "is_default_variant": true,
          "title": "my-title",
          "stock_quantity": 100,
          "stock_status": 1,
          "description": "Description text is here",
          "categories": [
              {
                  "cat_id": 1,
                  "cat_name": "Clothing"
              }
          ],
          "brand": "my-brand",
          "main_image_url": "https://test/image/link",
          "image_urls": [
              "www.image1.com",
              "www.image2.com"
          ],
          "product_link": "https://example.com/product/link/",
          "type": "variable",
          "status": 1,
          "regular_price": 100.00,
          "price": 99.00,
          "sale_price": 50.00,
          "cost_price": 0,
          "weight": 118.5,
          "colour": "green",
          "size": "large",
          "on_sale": false,
          "purchasable": false,
          "related_ids": [
              31
          ],
          "meta_fields": [
              {
                  "key": "country",
                  "value": "AUS",
                  "type": ""
              }
          ],
          "date_created_gmt": "2017-03-23T20:03:12",
          "date_modified_gmt": "2017-03-23T20:03:12"
      }
  ]
});

let config = {
  method: 'post',
  maxBodyLength: Infinity,
  url: 'https://example.com/product/upsert/',
  headers: { 
    'Content-Type': 'application/json', 
    'X-API-Key': 'meowmeowmeow'
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

This API is used to save the raw data into Warp Driven's data center for initialising and standardising products, and those product data will be fed for further AI services, such as **Visual similar**, **NLP-based Recommendation**, etc.

The product data should be attached to the POST Body part.

`X-API-KEY: meowmeowmeow`

### HTTP Request

`POST /product/upsert/`

### Request Body

Data | Description
--------- | -----------
items | The list of [product object](#product-property)

<aside class="notice">
For Authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

> Successful response example: 

```json
{
    "status": true,
    "msg": "Started Warp Driven Visual Search products init successfully.",
    "data": {
        "task_id": "{task_id}"
    }
}
```
```json
{
    "status": true,
    "msg": "There is no new product or updated product!",
    "data": {
        "task_id": null
    }
}
```

If you correctly add new products in the request body, and you have enabled the VS service, you should receive the task id in the response, which can be used to furtherly query the VS job status.

If you try to add the same products more than once, you will receive the response with nothing.

<aside class="success">
Our service is able to detect any product change in the attribute level, which means delta data. In this way, insert API should only be used to add new products or products with any attibutes change.
</aside>

## Update Products

> Example of how to update products:

```shell
```

```python
```

```javascript
```

This is the place to decribe the API

`X-API-KEY: meowmeowmeow`

### HTTP Request

`POST /product/update/`

### Request Body

Data | Description
--------- | -----------
update_items | The list of [product object](#product-property), but you can just list those changed attributes.

<aside class="notice">
First, the <code>shop_variant_id</code> is required!
Second, for authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

> Successful response example: 

```json
{
    "status": true,
    "msg": "Started Warp Driven Visual Search products init successfully.",
    "data": {
        "task_id": "{task_id}"
    }
}
```
```json
{
    "status": true,
    "msg": "There is no new product or updated product!",
    "data": {
        "task_id": null
    }
}
```

If you correctly add updated products in the request body, and you have enabled the VS service, you should receive the task id in the response, which can be used to furtherly query the VS job status.

If you try to add the same products more than once, you will receive the response with nothing.

## Delete Products

> Example of how to delete products:

```shell
curl --location --request DELETE 'https://example.com/product/delete/' \
--header 'Content-Type: application/json' \
--header 'X-API-Key: meowmeowmeow' \
--data '{
    "delete_shop_variant_ids": [
        "001", "002"
    ]
}'
```

```python
import requests
import json

url = "https://example.com/product/delete/"

payload = json.dumps({
  "delete_shop_variant_ids": [
    "001",
    "002"
  ]
})
headers = {
  'Content-Type': 'application/json',
  'X-API-Key': 'meowmeowmeow'
}

response = requests.request("DELETE", url, headers=headers, data=payload)

print(response.text)
```

```javascript
const axios = require('axios');
let data = JSON.stringify({
  "delete_shop_variant_ids": [
    "001",
    "002"
  ]
});

let config = {
  method: 'delete',
  maxBodyLength: Infinity,
  url: 'https://example.com/product/delete/',
  headers: { 
    'Content-Type': 'application/json', 
    'X-API-Key': 'meowmeowmeow'
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

This is the used to delete products from our services. To delete the product, you have to provide shop_variant_id.

`X-API-KEY: meowmeowmeow`

### HTTP Request

`POST /product/delete/`

### Request Body

Data | Description
--------- | -----------
delete_shop_variant_ids | The list of shop_variant_id 

<aside class="notice">
For authorization in the API header, you must replace the dummy <code>X-API-KEY</code> API key <code>meowmeowmeow</code> with your personal API key, which is assigned by Warp Driven.
</aside>

### Response

> Successful response example: 

```json
{
    "status": true,
    "msg": "{num_of_products} products have been successfully deleted!",
    "data": null
}
```

# Visually Similar Search API
