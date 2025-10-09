---
title: 'BigCommerce'
Description: 'BigCommerce Setup Guide'
---


6. Select an **Auth Scheme** and follow the relevant instructions below.

## Authentication Methods

### OAuth

The **Callback URL**, or Redirect URL, is the URL you need (``https://oauth.cdata.com/oauth/``) when setting up your OAuth app. Copy this URL and paste it into your OAuth app.

7. Enter the following information:
    
    - **OAuth Client Id**—the client Id assigned when you registered your Connect AI account for OAuth.

    - **OAuth Client Secret**—the client secret assigned when you registered your Connect AI account for OAuth.

    - **Store Id**—this is located in the BigCommerce URL when you are logged in to your account. It is formatted as `https://store-[StoreId].mybigcommerce.com/`.

### PersonalAccessToken

7. Enter the following information:

    - **OAuth Access Token**—To obtain the OAuth Access Token, log in to your BigCommerce account and do the following:
    
       1. Go to **Settings** > **Store-level API Tokens** > **+Create API Account**.
       2. Select **Token type** > **V2/V3 API Token**.
       3. Enter the name of your account (minimum of four characters).
       4. Choose the OAuth Scopes for the API Account you are creating. The driver cannot access data marked as "None" and cannot modify data marked as "read-only".
       5. Click **Save**. A successful save displays a pop-up window containing API credentials. Save your credentials, since you cannot return to this pop-up window. 

    - **Store Id**—this is located in the BigCommerce URL when you are logged in to your account. It is formatted as `https://store-[StoreId].mybigcommerce.com/`. In BigCommerce, it is also known as the store hash.
