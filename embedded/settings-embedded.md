---
layout: page
title: Settings
toc: true
level: 2
audiences: ["oem"]
---

You can access your *Settings* page by clicking the Gear Icon in the upper-right corner of the dashboard and selecting **Settings**. 

<img src="./assets/images/access_settings.png" width="200" />

The Settings page is divided into three tabs:

- **Profile**
- **Account**
- **Billing**

<img src="./assets/images/settings_tabs_embedded.png" width="350" />

The following sections describe these tabs.

## Profile

The **Profile** tab opens by default when you access Settings. This tab contains settings for the user that is currently logged in.

<img src="./assets/images/settings_profile_embedded.png" width="500" />

In the **User Profile** section, you can edit the first name and last name for the current user. You cannot edit the **Role**.

If you want to reset your password, click **Reset Password**. This action sends a password reset email to the email address that appears in **Email**.

## Account

The **Account** tab provides access to account-wide settings and troubleshooting features.

<img src="./assets/images/settings_account_embedded.png" width="500" />

The sections of this page are described below.

### General

The **General** section lists the following global account information:

- Organization Name
- Account Id
- Country

Copy the Account Id to use in the API.

Toggle **Display Connection Data Model** to show the Add and Edit Connection page for authenticated connections. 

### Primary Contact Information

This section contains the following fields that define the account's primary contact for invoices, announcements, and other communication:

- First name
- Last name
- Email
- Phone Number
- Country

### Delete Account

If you want to delete your {{ site.titlepowered }} account and all of its data, click **Contact Sales** for assistance.

**Notes:**
- Account deletion is permanent. If you delete your account, you need to create a new account if you want to use {{ site.titlepowered }} in the future.

## Billing

The **Billing** tab provides information and controls for your account plan and usage.

<img src="./assets/images/settings_billing_embedded.png" width="500" />

This tab consists of the following:

- The **Billing** section displays your plan information and next billing date.
- Click **Manage Payment Method** to open your account with Stripe. You can manage your billing settings, such as your payment method and billing address. If your subscription has lapsed, you need to reactivate your plan to continue using {{ site.titlepowered }}.
- The **Your Plan Includes** section displays what is included in your current plan.
- The lower pane displays your remaining usage in the plan.