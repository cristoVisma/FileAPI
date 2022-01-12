---
title: Authentication
sidebar: guides_sidebar
permalink: guides_authentication.html
folder: guides
---

{% include important.html content="The received token can be different based on the identity provider used" %}

We follow current industry standards and best practices. Authentication/authorization is no exception. As part of the Identity and Access Management Strategy for system-to-system integrations, our APIs are based OAuth 2.0 and the authorization grant Client Credentials. Every API consumer system will be provisioned in our API Gateway as a Client Application (App). Client ID and Client Secret will be provided to be used by Apps as credentials. Thus, Apps will be able then to authenticate and get an access token (JWT) within the response payload. Subsequent requests authorization will be based on that access token previously retrieved.


## Survey of features

Some of the more prominent features of this theme include the following:

* Bootstrap framework
* [Navgoco multi-level sidebar](http://www.komposta.net/article/navgoco) for table of contents
* Ability to specify different sidebars for different products
* Top navigation bar with drop-down menus
* Notes, tips, and warning information notes
* Tags for alternative navigation
* Advanced landing page layouts from the [Modern Business theme](http://startbootstrap.com/template-overviews/modern-business/).

## Getting started

To get started, see [Getting Started][index].

{% include links.html %}
