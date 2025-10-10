---
title: "Salesforce"
description: "Salesforce Setup Guide"
---

import MySnippet from '/snippets/source-intro.mdx';

## Required Prerequisites (Salesforce Admin Only)

1. In Connect AI Setup, navigate to **Apps** \> **Connected Apps** \> **Connected Apps OAuth Usage**.
2. For the CData Connector, click **Install**. Salesforce displays an installation page.
3. Click **Install** again to complete the process.
5. Select the Authentication method, then proceed to the relevant section and follow those instructions.

<MySnippet page="Salesforce" />

## Authentication Methods

<Accordion title="Basic">
### Basic

3. Enter a security token. This step is mandatory unless your IP has been added to 'Trusted IP Addresses' in Salesforce already.
4. Set the **Use Sandbox** field to **True** (if you are connecting to a sandbox account). Otherwise, leave it as **False**.
</Accordion>

### OAuth

1. Set the **Use Sandbox** field to **True** (if you are connecting to a sandbox account). Otherwise, leave it as **False**.

### OAuthPassword

3. Enter a **Security Token**. This step is mandatory unless your IP has been added to 'Trusted IP Addresses' in Salesforce already.
4. Set the **Use Sandbox** field to **True** (if you are connecting to a sandbox account). Otherwise, leave it as **False**.

### OAuthJWT

1. Enter your **OAuth JWT Certificate**. This is multi-line and in PEM format.
2. Select the **OAuth JWT Certification type**.
3. Enter the **OAuth JWT Issuer**. This must include the client_id or connected app for the which the certificate is registered.
4. (Optional) Enter an **OAuth JWT Cert Password** if the certificate. This only needs to be done if the certificate is encrypted.
5. (Optional) If required, add an **OAuth JWT Cert Subject**.
6. (Optional) If implementing for an Experience Cloud Site, an **OAuth JWT Subject** is required. It must be formatted as an email.
7. Set the **Use Sandbox** field to **True** (if you are connecting to a sandbox account). Otherwise, leave it as **False**.

### OneLogin

1. Enter the OneLogin **User** Id.
2. Add the **Password** for that account.
3. Enter the **SSO Properties**, with the format 'ssoproperty1=value1;sooproperty2=value2;sooproperty3=value3;'. Make sure to separate all property-value pairs with semicolons.
4. Add the **SSO Exchange URL** You can find this in the Salesforce account settings by navigating to **Administration Setup \> SAML Single Sign-On Settings** and locating the OAuth 2.0 Token endpoint.
5. Set the **Use Sandbox** field to **True** (if you are connecting to a sandbox account). Otherwise, leave it as **False**.

### PingFederate

1. Enter the PingFederate **User** Id.
2. Add the **Password** for that account.
3. Enter the **SSO Properties**, with the format 'ssoproperty1=value1;sooproperty2=value2;sooproperty3=value3;'. Make sure to separate all property-value pairs with semicolons.
4. Add the **SSO Exchange URL** You can find this in the Salesforce account settings by navigating to **Administration Setup \> SAML Single Sign-On Settings** and locating the OAuth 2.0 Token endpoint.
5. Set the **Use Sandbox** field to **True** (if you are connecting to a sandbox account). Otherwise, leave it as **False**.

### OKTA

1. Enter the OKTA **User** Id.
2. Add the **Password** for that account.
3. Enter the **SSO Properties**, with the format 'ssoproperty1=value1;sooproperty2=value2;sooproperty3=value3;'. Make sure to separate all property-value pairs with semicolons.
4. Add the **SSO Exchange URL** You can find this in the Salesforce account settings by navigating to **Administration Setup \> SAML Single Sign-On Settings** and locating the OAuth 2.0 Token endpoint.
5. Set the **Use Sandbox** field to **True** (if you are connecting to a sandbox account). Otherwise, leave it as **False**.

### ADFS

1. Enter the ADFS **User** Id.
2. Add the **Password** for that account.
3. Enter the **SSO Properties**, with the format 'ssoproperty1=value1;sooproperty2=value2;sooproperty3=value3;'. Make sure to separate all property-value pairs with semicolons.
4. Add the **SSO Exchange URL** You can find this in the Salesforce account settings by navigating to **Administration Setup \> SAML Single Sign-On Settings** and locating the OAuth 2.0 Token endpoint.
5. Set the **Use Sandbox** field to **True** (if you are connecting to a sandbox account). Otherwise, leave it as **False**.

### AzureAD

1. Enter the **SSO Properties**, with the format 'ssoproperty1=value1;sooproperty2=value2;sooproperty3=value3;'. Make sure to separate all property-value pairs with semicolons.
2. Add the **SSO Exchange URL** You can find this in the Salesforce account settings by navigating to **Administration Setup \> SAML Single Sign-On Settings** and locating the OAuth 2.0 Token endpoint.
3. Enter the **OAuth Client Id** assigned when you registered your Salesforce account for OAuth.
4. Enter the **OAuth Client Secret** for your Salesforce account for OAuth.
5. Set the **Use Sandbox** field to **True** (if you are connecting to a sandbox account). Otherwise, leave it as **False**.