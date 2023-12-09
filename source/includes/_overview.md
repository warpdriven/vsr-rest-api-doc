# Overview

WarpDriven Services can be splitted into 3 parts: ERP, customer management service and data/AI services (Nuwa, Visual Search and NLP)

<img alt="alt_text" width="auto" src="https://github.com/warpdriven/vsr-rest-api-doc/blob/dev/images/overview.png?raw=true"/>

## ERP Workflow

Our ERP system is used to manage the user account. You should register a WarpDriven account and subscribe the plan before integrating your services or using our APIs.

To register a WarpDriven account, please go to our [offical website](https://warp-driven.com). You will also need to choose a plan and subscribe it, and check it from [here](https://erp.warp-driven.com/@/subscription).


### <a id="plan-id">About Plan ID</a>

When you choose the plan, there are a few options.We are using **plan id** in our API to represent each plan.

Plan Name | Plan ID
--------- | --------
Visual Search | 1
NLP | 11

### Workflow

The workflow graph is below:

<img alt="alt_text" width="auto" src="https://github.com/warpdriven/vsr-rest-api-doc/blob/dev/images/erp.png?raw=true"/>


## Customer Management Service Workflow

### Workflow

The workflow graph is below:

<img alt="alt_text" width="auto" src="https://github.com/warpdriven/vsr-rest-api-doc/blob/dev/images/customer-mgt-service.png?raw=true"/>

## Authorization

Usually, if you successfully created your account, subscribed to the plan, and created the website, you should be able to get the unique API key, which is assigned by WarpDrive. Ideally, You can call any API in the document.

<aside class="notice">
For Authorization, in any API example, you must replace the dummy <code>X-API-KEY</code> API key in the header with your personal API key, which is assigned by WarpDriven.
</aside>

## Nuwa Workflow

Nuwa is WarpDriven's data storage service. All your products should go through the Nuwa, and Nuwa will save your data into our database. It will also assign the data calculating related jobs to other services. For example, it will launch **Visual Search** jobs if you also require the visual search plan.

<aside class="success">
Nuwa is able to capture the data change for data update and insert every time and charge the credit appropriately.
</aside>

## Visual Search Workflow

Visual Search service will be triggered once new product images are coming. This service will automatically calculate the image vector and related features for each new product image. 

Those data will be used to support our AI model and visual search engine.