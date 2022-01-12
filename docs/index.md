---
title: "File API Introduction"
keywords: sample homepage
tags: [getting_started]
sidebar: guides_sidebar
permalink: index.html
summary: The File API allows you to download or upload files directly from Youforce, over HTTPS using the tool of your choice.
---


{% include important.html content="This API is controlled available and has consumption limitations. See API <a href='https://community.raet.com/developers-community/w/youforce-apis/2763/api-statuses'>statuses</a>." %}

## Authentication

We follow current industry standards and best practices. Authentication/authorization is not an exception. As part of the Identity and Access Management Strategy for system-to-system integrations, the File API is based on OAuth 2.0 and the authorization grant Client Credentials. Every API consumer system will be provisioned in our API Gateway as a Client Application (App). Client ID and Client Secret will be provided to be used by Apps as credentials. Thus, Apps will be able then to authenticate and get an access token (JWT) within the response payload. Subsequent requests authorization will be based on that access token previously retrieved.

## Tenant Authorization
Client Applications need to be authorized to the corresponding Tenant (HR Core Client) in order to consume the API.
By default, the applications are authorized to TenantId: **sandbox**. 


## File Type Authorization

The files which are related to the same “business” are functionally grouped in File types called **Business types**. Business Types are represented by an integer called Business Type Id.
Client applications (apps) need to be authorized as publisher or subscriber of business types

* Publisher is an application that uploads files to be consumed for other subscribers
* Subscriber is an application that downloads the files provided by other publisher. 

By default, the client Apps are authorized to the Sandbox File Types: 

| Business Type Id | Name | Authorization |
|--------|---------|---------|
| 7100 | File API Sandbox Uploads | Publisher
| 7101 | File API Sandbox Downloads | Subscriber

## Supported File Types

The File API has been designed to support a specific set of use cases. This may be extended over time, based on customer feedback. See list of [Supported File Types](https://community.raet.com/developers-community/w/file-api/2396/file-supported-file-types).

## Curl Example

Here is an example of downloading a file using curl, available on most operating systems: 

```
curl.exe https://api.raet.com/mft/v1.0/files/%fileid%?role=subscriber ^
--header "Authorization: Bearer eyJhbGciOiJSUzI1NiIs..." ^
--header "x-raet-tenant-id: 1234567" ^
--header "Accept: application/octet-stream"  ^
--output @C:\Youforce\somefile.xml
```

See complete [examples](https://github.com/transportersteam/FileAPI.Integration.Examples) for curl (Batch), Powershell and .Net in Github. 

