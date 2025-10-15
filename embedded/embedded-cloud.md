---
title: Quick Start Guide
---

Embedded Cloud is a way for customers to integrate Connect AI live data access capabilities for their end users within their own applications. 

Contact CData sales if you are interested in an Embedded Cloud account.

Embedded Cloud consists of two levels of accounts:

- **Parent Account**—CData sales creates the parent account. The parent account is responsible for managing the child accounts and can create, view, and edit child accounts through the Embedded Cloud API. The parent account can monitor and troubleshoot child accounts.

- **Child Account**—In the child account, each end user will have his/her own account. The end users can create, edit, and delete data sources. They can connect to data sources and query data.

The **Accounts** tab contains the child account names and Ids for reference.

Click a child account to view the child account's connections.

The **Users** tab displays the authorized users of the parent Embedded Cloud account.

Note that users of Embedded Cloud cannot access all the features of Connect AI. 

## Quickstart

The following is an overview of setting up Embedded Cloud. There are four main steps.
  
### Step 1: Create a Parent Account

1. The administrator of the Embedded Cloud parent account [creates a JSON Web Token (JWT)](./Authentication-Embedded.html), which consists of a private key and a corresponding public key. The private key must be stored according to the security requirements of the product integrated with Embedded Cloud.

2. The administrator provides the public key certificate in Privacy-Enhanced Mail (PEM) format to register the management account. They can register the public key by opening a support ticket with Embedded Cloud.

3. Once registered, the administrator of the parent account can sign in to the account. Please accept the terms of service.

### Step 2: Create a Child Account

Use [Create Account](./Account-API.html#create-account) in the Embedded Cloud API to create a child account. You must supply the JWT that you created in [Create a Parent Account](#create-a-parent-account).

### Step 3: Configure a Connection

An end user of the child account clicks **Add Connection** on your web page. On the backend, your web site calls the Create Connnection API, which generates a redirect URL to the Embedded Cloud web page. The end user can then configure a connection of a certain type, such as a Salesforce connection, and save and test the connection. When the end user is finished, he/she is then redirected back to your web page containing a list of connections. See [Connection Flow](./Connection-Flow.html) for more details.

### Step 4: Query the Data

Use one of the following Connect AI drivers to query the data:

- [ADO.NET](./ADO.NET-Client.html)
- [ODBC](./ODBC-Client.html)
- [JDBC](./JDBC-Client.html)
- [Python](./Python-Client.html)

In addition, Embedded Cloud provides a full-featured [REST API](./REST-API.html). You can query data directly with any REST-compatible application or integration tool capable of creating HTTP requests.

### View Logs

Use the [Log API](./Log-API.html) to view and download a list of logs for an Embedded Cloud account.   