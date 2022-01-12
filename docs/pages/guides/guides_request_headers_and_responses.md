---
title: Request headers and responses
sidebar: guides_sidebar
permalink: guides_request_headers_and_responses.html
folder: guides
---

## Request headers

| Header Name| Description |
|--------|---------|
| Cache-Control | The Cache-Control general-header field is used to specify directives that MUST be obeyed by all caching mechanisms along the request/response chain. In our authentication request the header is mandatory with the value. **Cache-Control: no-cache**|
| Content-Type | The content type of the resource in case the request has content in the body. Example: **Content-Type:multipart/related;boundary=foo_bar_baz**|
| Authorization | The information required for authentication |
| Accept | The Accept request-header can be used to specify the media types which are acceptable for the response. Example: **Accept:application/octet-stream**|
| x-raet-tenant-id | This header is used to specify for which tenant the data is requested. For tokens with single tenant access, this header is not mandatory. Example: **x-raet-tenant-id: 1234567**|
