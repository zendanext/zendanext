---
layout: post
title:  "Welcome to ZendaNext!"
date:   2024-09-27 08:57:24 +0200
categories: jekyll update
---


ZendaNext enables simple SQL access to complex, secured, asynchronous JSON APIs.

```sql
D SELECT name, address, occupation FROM rest_api("my_rest_api", auth=true, max_concurrent_requests=10);
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

