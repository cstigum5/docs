---
layout: page
title: Quick Start Guide
audiences: ["oem"]
toc: true
level: 3
---

{{ site.titlepowered }} is a way for customers to integrate {{ site.title }} live data access capabilities for their end users within their own applications. 

Contact CData sales if you are interested in a {{ site.titlepowered }} account.

{{ site.titlepowered }} consists of two levels of accounts:

- **Parent Account**—CData sales creates the parent account. The parent account is responsible for managing the child accounts and can create, view, and edit child accounts through the {{ site.titlepowered }} API. The parent account can monitor and troubleshoot child accounts.

- **Child Account**—In the child account, each end user will have his/her own account. The end users can create, edit, and delete data sources. They can connect to data sources and query data.

The {{ site.titlepowered }} **Accounts** tab contains the child account names and Ids for reference.

<img src="./assets/images/powered_by_cdata_accounts.png" width="600" />	

Click a child account to view the child account's connections.

The {{ site.titlepowered }} **Users** tab displays the authorized users of the parent {{ site.titlepowered }} account.

<img src="./assets/images/powered_by_cdata_users.png" width="600" />	

Note that users of {{ site.titlepowered }} cannot access all the features of {{ site.title }}. 

## {{ site.titlepowered }} Quickstart

The following is an overview of setting up {{ site.titlepowered }}. There are four main steps.
  
### Step 1: Create a Parent Account

1. The administrator of the {{ site.titlepowered }} parent account [creates a JSON Web Token (JWT)](./Authentication-Embedded.html), which consists of a private key and a corresponding public key. The private key must be stored according to the security requirements of the product integrated with {{ site.titlepowered }}.

2. The administrator provides the public key certificate in Privacy-Enhanced Mail (PEM) format to register the management account. They can register the public key by opening a support ticket with {{ site.title }}.

3. Once registered, the administrator of the parent account can sign in to the account. Please accept the terms of service.

### Step 2: Create a Child Account

Use [Create Account](./Account-API.html#create-account) in the {{ site.titlepowered }} API to create a child account. You must supply the JWT that you created in [Create a Parent Account](#create-a-parent-account).

### Step 3: Configure a Connection

An end user of the child account clicks **Add Connection** on your web page. On the backend, your web site calls the Create Connnection API, which generates a redirect URL to the {{ site.titlepowered }} web page. The end user can then configure a connection of a certain type, such as a Salesforce connection, and save and test the connection. When the end user is finished, he/she is then redirected back to your web page containing a list of connections. See [Connection Flow](./Connection-Flow.html) for more details.

### Step 4: Query the Data

Use one of the following {{ site.title }} drivers to query the data:

- [ADO.NET](./ADO.NET-Client.html)
- [ODBC](./ODBC-Client.html)
- [JDBC](./JDBC-Client.html)
- [Python](./Python-Client.html)

In addition, {{ site.titlepowered }} provides a full-featured [REST API](./REST-API.html). You can query data directly with any REST-compatible application or integration tool capable of creating HTTP requests.

### View Logs

Use the [Log API](./Log-API.html) to view and download a list of logs for a {{ site.titlepowered }} account.   