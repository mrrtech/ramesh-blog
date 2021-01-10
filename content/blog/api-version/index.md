---
title: What is the correct way to version my API?
date: "2021-01-01T22:12:03.284Z"
description: ""
---

The "URL" way

A commonly used way to version your API is to add a version number in the URL. For instance:

```
/api/v1/article/1234

```

To "move" to another API, one could increase the version number:

```
/api/v2/article/1234

```

The hypermedia way

```
GET /api/article/1234 HTTP/1.1
Accept: application/vnd.api.article+xml; version=1.0

```
