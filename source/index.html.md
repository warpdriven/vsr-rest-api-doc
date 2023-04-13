# Warp Driven Nuwa (女娲) Platform API
Welcome to Warp Driven Nuwa Platform API docs

## Version: 1.0

### /product/upsert

#### POST
##### Summary

Upsert

##### Description

Init VS products with item JSON format input\\n\\nArgs:\\n\\n    items_info: product_ids, is_convert_webp, is_remove_background, data_checkpoints\\n\\n    website_info: input api_key top get website info\\n\\nReturns:\\n\\n    success_response_handler or error_response_handler

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful Response |
| 422 | Validation Error |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| APIKeyHeader |  |

### /product/update

#### POST
##### Summary

Update

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful Response |
| 422 | Validation Error |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| APIKeyHeader |  |

### /product/delete

#### DELETE
##### Summary

Delete

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful Response |
| 422 | Validation Error |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| APIKeyHeader |  |

### /product/get_vs_credit_status

#### GET
##### Summary

Get Vs Credit Status

##### Description

Get VS init process status\\n\\nReturns:\\n\\n    {\\n\\n        \\"status\\": True,\\n\\n        \\"msg\\": msg,\\n\\n        \\"data\\": {\\n\\n            'task_id': <task_id>,\\n\\n            'task_status': 'RUNNING,\\n\\n            'task_progress': 60,\\n\\n            'is_expired': false,\\n\\n            'plan_end_time': '2023-10-24',\\n\\n            'image_vector_left': 10,\\n\\n            'webp_left': 100,\\n\\n            'bk_rm_left': 100\\n\\n        }\\n\\n    }

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ------ |
| plan_id | query |  | Yes | integer |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful Response |
| 422 | Validation Error |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| APIKeyHeader |  |

### /product/init_bigdata/

#### POST
##### Summary

Init Products Bigdata

##### Description

Init VS products with product IDs for big data items init\\n\\nArgs:\\n\\n    items_info: product_ids, is_convert_webp, is_remove_background, data_checkpoints\\n\\n    website_info: input api_key top get website info\\n\\nReturns:\\n\\n    success_response_handler

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful Response |
| 422 | Validation Error |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| APIKeyHeader |  |

### /product/reload

#### POST
##### Summary

Reload Data

##### Description

Reload data into ElasticSearch for dev using

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful Response |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| APIKeyHeader |  |

### /product/handle_history

#### GET
##### Summary

Show Products Handle History

##### Description

Get website products image handle history list

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ------ |
| page_no | query |  | No | integer |
| page_size | query |  | No | integer |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful Response |
| 422 | Validation Error |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| APIKeyHeader |  |
