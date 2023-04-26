# Overview

## ERP Workflow

Our ERP system is used to manage the user account. You should register a WarpDriven account and subscribe the plan before integrating your services or using our APIs.

To register a WarpDriven account, please go to our [offical website](https://warp-driven.com). You will also need to choose a plan and subscribe it, and check it from [here](https://erp.warp-driven.com/@/subscription).


### <a id="plan-id">About Plan ID</a>

When you choose the plan, there are a few options.We are using **plan id** in our API to represent each plan.

Plan Name | Plan ID
--------- | --------
Visually Similar Recommendation | 1
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

## Visually Similar Recommendation Workflow