# Poq.Sfcc.Checkout.Bridge.Cartridge

## Current Version 19.1.0

### Table of Contents

1. [Summary](#summary)
2. [Component Overview](#component-overview)
    1. [Functional Overview](#functional-overview)
    2. [Limitations, Constraints](#limitations-constraints)
    3. [Compatibility](#compatibility)
    4. [Privacy, Payment](#privacy-payment)

3. [Implementation Guide](#implementation-guide)
    1. [Setup](#setup)
    2.  [Configuration](#configuration)
    4.  [External Interfaces](#external-interfaces)
    5.  [Testing](#testing)
        1.  [Steps](#steps)
    3.  [Unit tests](#unit-tests)

4.  [Operations, Maintenance](#operations-maintenance)
    1.  [Data Storage](#data-storage)
    2.  [Support](#support)

5.  [User Guide](#user-guide)
    1.  [Roles, Responsibilities](#roles-responsibilities)

6.  [Known Issues](#known-issues)
7.  [Release History](#release-history)

------------------------------
## Summary

*   Poq is a certified Salesforce Premier LINK Technology Partner. LINK Technology Partners offer value-added products and innovations that integrate with and complement Commerce Cloud. Using the Poq platform, retailers retain full creative control of their apps, whilst inventory, orders and customer accounts are seamlessly integrated with Commerce Cloud.

*   This means that retailers on Commerce Cloud can quickly and easily integrate an app built on the Poq platform with their main e-commerce website without replicating inventory and processes.

*   The Checkout LINK cartridge from Commerce Cloud can be installed and used for a checkout analisys integration with Poq. It speeds up integration of Poq [Web Checkout](https://docs.poqcommerce.com/integrations/cart-transfer-guide/web-checkout).

------------------------------

## 2.   Component Overview

### 2.1.   Functional Overview

This cartridge provides [Web Checkout](https://docs.poqcommerce.com/integrations/cart-transfer-guide/web-checkout) integration with Poq platform.

### 2.2.   Limitations, Constraints

 This integration is tested only on default checkout process and pages for SG and SFRA. Integration with heavily customized sites should be done with caution.

### 2.3.   Compatibility

Cartridge should be generally compatible with all versions of Site Genesis, however it was built and tested under 14.6.0.15 version of Site Genesis.

### 2.4.   Privacy, Payment

No credit card info is stored in Salesforce Commerce Cloud, all of the orders are transferred back to Salesforce Commerce Cloud via Poq API before the checkout process.

------------------------------

## 3.   Implementation Guide

### 3.1.   Setup

Before you start please make sure the cartridge ``int_poq_checkout_bridge`` is added to the Business Manager cartridge path, and Site Cartridge path.

### 3.2.   Configuration

Cartridge does not require any specific configuration.

### 3.4.   External Interfaces

No external interfaces are defined for this integration.

### 3.5.   Testing

Testing accounts can be requested from Poq Commerce.

#### Steps

1.  Upload cartridge to your instance;
2.  Configure cartridge in ``Administration >  Sites >  Manage Sites > Site - Settings -> Cartridges``
3.  Activate latest version from ``Administration >  Site Development >  Code Deployment``
4.  Proceed to checkout with Poq app.
5.  Verify that webview is closed after clicking `continue shopping`.
6.  Verify in analitics that event for your order was sent to Poq.

### 3.5.3. Unit tests

Unit tests can be run by first installing the package dependencies with ``npm install`` , then run them with ``npm run test``

The coverage is towards the generation of data from a mock product, and wether the code produces the correct CSV line data, with all columns, including configurable custom ones.

## Requirements

* The code can run under SiteGenesis and SFRA 4.3.0+

------------------------------

## 4.   Operations, Maintenance

### 4.1.   Data Storage

    There is no custom storage of data.

### 4.2. Support

------------------------------
Should there be a service failure or unexpected downtime, Poq should be contacted. In case of problems with the connection to Poq, please use contact as below

Email at [support@poqcommerce.com](mailto:support@poqcommerce.com) or by phone at [+442037944120](tel:+442037944120)

## 5.   Release History

| Version | Date | Changes |
| --- | --- | --- |
|1.0.0 | 18 June 2021 | Initial release |
