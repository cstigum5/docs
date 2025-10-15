---
layout: page
title: Quick Start Guide
audiences: ["standard"]
toc: true
level: 3
---

Connect a data source, explore it, and use it from AI or BI tools—in minutes.

## Step 1: Sign In

1. Go to [https://cloud.cdata.com/](https://cloud.cdata.com){:target="_blank"}.
2. Sign in with your CData account. 

*No account? Click **Sign Up** for a free trial.*

## Step 2: Connect Your First Source

### Example: Salesforce (OAuth)

1. Open **Sources** > **Add Connection** > **Salesforce**.
2. Select **OAuth** authentication (recommended).
3. Provide:
   - **Client ID** and **Client Secret** from Salesforce (*Setup > App Manager > Your Connected App*).
   - **Callback URL** shown in {{ site.title }}.
4. Click **Authorize** and sign in with Salesforce.
5. **Test** connection, and then **Save**.

***Done!*** *You can now query `Account`, `Opportunity`, `Contact`, and other objects in real time.*

### Example: Google BigQuery (OAuth)

1. Open **Sources** > **Add Connection** > **Google BigQuery**.
2. Sign in with your Google account.
3. Select the project and dataset(s) to expose.
4. Test connection, and Save.

   *Your BigQuery datasets are now queryable via SQL, OData, and REST.*

*Other authentication options include Username/Password (legacy) and OAuth with Refresh Token for long-lived access.*   

## Step 3: Explore and Query Your Data

1. Open **Explorer** and select your source.
2. Run a query: 
   ```sql
   SELECT Name, StageName, Amount
   FROM Opportunity
   WHERE CloseDate >= CURRENT_DATE - 90
   ORDER BY Amount DESC;
   ```

*Save as a ***Derived View*** to reuse and share.*   

## Step 4: Create Derived Views

Derived Views are saved SQL definitions you can permission like tables.

```sql
CREATE DERIVED VIEW Sales.TopOpportunities AS
SELECT Name, StageName, Amount
FROM Opportunity
WHERE IsClosed = false AND CloseDate >= CURRENT_DATE - 90
ORDER BY Amount DESC
LIMIT 10;
```

*Use ***Scheduled Queries*** under ***Jobs*** to refresh cached results for heavy workloads.*

## Step 5: Use Data in Your Tools

### Power BI (SQL endpoint)
1. Open Power BI Desktop and then select **Get Data** > **SQL Server**.
2. Enter your Connect Cloud SQL endpoint (*tds.cdata.com*).
3. Authenticate with your CData credentials.
4. Select tables or derived views and build visuals.

### Excel (OData)

1. In Excel, select **Data** > **Get Data** > **From Other Sources** > **From OData Feed**.
2. Paste your Connect Cloud OData endpoint (*https://cloud.cdata.com/api/odata/{workspace_name}*).
3. Authenticate with your CData credentials and load data.

### Tableau (OData or SQL)

1. In Tableau, select **Connect** > **OData Server** (or **SQL Server**).
2. Enter either the OData or SQL Server endpoint, authenticate, and start exploring.

### AI and Apps (Rest/OpenAPI)

Expose any source as a secure API for custom apps and large language models (LLMs).

- REST provides programmatic access from apps/agents:

  ``
  GET https://cloud.cdata.com/api.rsc/Salesforce/Opportunity
  Authorization: Bearer <token>
  ```

- OData v4 is used for BI tools and pagination/filtering:

  ```
  GET https://cloud.cdata.com/odata/Salesforce/Opportunity?$top=100&$orderby=Amount desc
  ```

- OpenAPI generates clients and validates requests:

  ```  
  GET https://cloud.cdata.com/openapi/Salesforce
  ```

## Step 6: Organize with Workspaces

1. In Workspaces, **Add Workspace** and name the workspace (for example, Sales).
2. Add sources and derived views needed by the team.
3. Share with groups to grant access.

## Step 7: Permissions by Need-to-Know

Control access at source, schema, table, or view level

**Permission** | **What it allows** 
SELECT | Read/query data 
INSERT/UPDATE/DELETE | Write changes back (if source allows)
EXECUTE | Run procedures (such as refresh metadata)

## Security and Best Practices

- **Rate limits**: 100 requests/user/minute.
- **IP allowlist**: Restrict access to trusted networks.
- **Logging & audit**: Enable detailed logs for governance.

## Troubleshooting

*Connection failed? Verify credentials, network/VPN, and source API status.*

- **Missing tables?** Refresh metadata on the source.
- **Slow queries?** Filter early, limit columns, and enable caching.
- **Auth errors?** Re-authorize OAuth and confirm scopes.

{% include_relative common-gs-techsupport.md %}

## What's New

See our [Release Notes](./ReleaseNotes.html) for new connectors, enhancements, and fixes.