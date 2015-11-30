---
layout: api
title: API - Categories
sidebar: api
lang: en
subnav: api_c_categories

description:
    - Read the categories

methods:
    - { name: GET, route: /api/categories, return_code: 200, return: "Results of the 'category' loop" }
    - { name: GET, route: "/api/categories/{entityId}", parameters: "entityId: The category id", return_code: 200, return: "Results of the 'category' loop for entityId" }
---
---


## Creation

If you want to create a category, you have to send the following fields with the POST method.

##### General information

- parent  : The parent category id or 0
- visible  : If true, the category will be visible (optional)

##### Descriptive

- locale: The lang locale
- title: The product title

### Example
```json
{
    "locale": "en_US",
    "title": "category create from api",
    "parent": 12,
    "visible": 1
}
```

## Update

##### General information

- parent  : The parent category id or 0
- visible  : If true, the category will be visible (optional)
- default\_template\_id   : The template id (optional)

##### Descriptive

- locale: The lang locale
- title: The category title
- chapo: The category short description (optional)
- description: The category description (optional)
- postscriptum: The category conclusion (optional)

To update a category, you have to send the same data (only updated ones) as for a create, but with the PUT method.

### Example
```json
{
    "locale": "en_US",
    "title": "category create from api",
    "description": "category description from api",
    "parent": 12,
    "visible": 1
}
```