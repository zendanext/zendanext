---
layout: post
title:  "Welcome to ZendaNext!"
date:   2024-09-27 08:57:24 +0200
categories: jekyll update
---


ZendaNext enables simple SQL access to complex, secured, asynchronous JSON APIs.

```sql
D SELECT name, address, occupation FROM zenda("my_rest_api", auth=true, max_concurrent_requests=10);
┌────────────────┬────────────────┬────────────┐
│      name      │    address     │ occupation │
│    varchar     │    varchar     │  varchar   │
├────────────────┼────────────────┼────────────┤
│ John Doe       │ 123 Main St    │ Engineer   │
│ Jane Smith     │ 456 Oak St     │ Designer   │
│ Sam Johnson    │ 789 Pine St    │ Teacher    │
│ Emily Davis    │ 101 Birch St   │ Artist     │
│ Michael Lee    │ 202 Cedar St   │ Developer  │
│ Linda Brown    │ 303 Maple St   │ Scientist  │
│ David Wilson   │ 404 Spruce St  │ Consultant │
│ Susan Martinez │ 505 Oak St     │ Manager    │
│ Robert Clark   │ 606 Elm St     │ Analyst    │
│ Karen Lewis    │ 707 Willow St  │ Accountant │
│ Nancy Robinson │ 1010 Forest St │ Retired    │
│                │                │            │
├────────────────┴────────────────┴────────────┤
│ 12 rows                            3 columns │
└──────────────────────────────────────────────┘
```


### config


```json
[
    {
        "name": "peeps",
        "config": {
            "host": "localhost",
            "port": 3000,
            "root_uri": "",
            "endpoints": {
                "data": {
                    "uri": "data"
                },
                "schema": {
                    "uri": "schema"
                }
            },
            "async": {
                "submit": {
                    "method": "POST",
                    "uri": "async/submit",
                    "headers": [
                        {
                            "key": "Authorization",
                            "value": "Bearer YOUR_TOKEN"
                        },
                        {   "key": "Content-Type",
                            "value": "application/json"
                        }
                    ]
                },
                "check": {
                    "method": "GET",
                    "uri": "async/check/{id}",
                    "params": [
                        {
                            "key": "id",
                            "value": "{id}"
                        }
                    ]
                },
                "fetch": {
                    "method": "GET",
                    "uri": "async/fetch/{id}",
                    "params": [
                        {
                            "key": "id",
                            "value": "{id}"
                        }
                    ]
                }
            }
        }
    },
    {
        "name": "animals",
        "config": {
            "host": "freetestapi.com",
            "port": 443,
            "root_uri": "api",
            "endpoints": {
                "data": {
                    "uri": "v1/animals"
                },
                "schema": {
                    "uri": "site/animals"
                }
            }
        }
    },
    {
        "name": "cars",
        "config": {
            "host": "freetestapi.com",
            "port": 443,
            "root_uri": "api",
            "endpoints": {
                "data": {
                    "uri": "v1/cars"
                },
                "schema": {
                    "uri": "site/cars"
                }
            },
            "schema": [
                {
                    "name": "id",
                    "type": "number"
                },
                {
                    "name": "make",
                    "type": "string"
                },
                {
                    "name": "model",
                    "type": "string"
                },
                {
                    "name": "year",
                    "type": "number"
                },
                {
                    "name": "color",
                    "type": "string"
                },
                {
                    "name": "mileage",
                    "type": "number"
                },
                {
                    "name": "price",
                    "type": "number"
                },
                {
                    "name": "fuelType",
                    "type": "string"
                },
                {
                    "name": "transmission",
                    "type": "string"
                },
                {
                    "name": "engine",
                    "type": "string"
                },
                {
                    "name": "horsepower",
                    "type": "number"
                },
                {
                    "name": "features",
                    "type": "array"
                },
                {
                    "name": "owners",
                    "type": "number"
                },
                {
                    "name": "image",
                    "type": "string"
                }
            ]
        }
    }
]
```