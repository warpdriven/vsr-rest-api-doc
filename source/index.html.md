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

# Nuwa

# Visually Similar Search
