# Source: https://docs.cfo.ai/integrations/connect-and-sync-data

Integrations bring financial and operating data into your cfo.ai Model. Connect a source when real accounting, people, customer, or spreadsheet history should inform your analysis.

## 

[​](https://docs.cfo.ai/integrations/connect-and-sync-data#choose-the-right-source)

Choose the right source

Common starting points include:

- Accounting systems such as QuickBooks Online, Xero, or NetSuite.
- HR and payroll systems such as Rippling, Gusto, BambooHR, or Workday.
- CRM systems such as HubSpot or Salesforce.
- Google Sheets or a PostgreSQL-compatible database.
- A CSV or another supported file-upload flow for a source that is not connected directly.

Available sources and plan entitlements can vary. Ask Ari to check the catalog for the system you use.

## 

[​](https://docs.cfo.ai/integrations/connect-and-sync-data#connect-a-business-system)

Connect a business system

1

Tell Ari what you want to connect

Name the source and what you want to use it for.

> Connect QuickBooks Online so we can build a monthly profit and loss statement.

2

Approve the connection

Ari opens or links you to the connection flow. Complete the sign-in and approval in your browser. Ari cannot enter your password or approve access for you.

3

Wait for the initial load

cfo.ai starts loading the connected data after the source links. The import can continue in the background while you work on something else.

4

Check what arrived

Ask Ari whether the connection has finished, when data was last loaded, and which information is ready for analysis.

> Check whether QuickBooks finished syncing and tell me which accounting periods are available.

## 

[​](https://docs.cfo.ai/integrations/connect-and-sync-data#upload-a-file)

Upload a file

If you attach a CSV in Ari chat, choose whether it should become a data source or stay attached only to the conversation.

- **Use as a data source** when the file’s rows should become available in the Model.
- **Use in chat only** when Ari should read or summarize the file without importing it.

An uploaded data source is identified by its filename until you rename it. If the same filename already backs a connection, cfo.ai asks for confirmation before replacing it. If the file is an existing financial model rather than a source-data export, ask Ari to [import and rebuild the spreadsheet model](https://docs.cfo.ai/getting-started/import-a-spreadsheet-model) instead of treating the workbook as an ordinary data connection.

## 

[​](https://docs.cfo.ai/integrations/connect-and-sync-data#understand-sync-status)

Understand sync status

A connected source is ready only after its background load completes. A linked account, started import, or uploaded file does not by itself mean the resulting data is already available. If the Model contains fewer rows than the source file, ask Ari which source records were included. A saved query may intentionally filter the source to match your request.

## 

[​](https://docs.cfo.ai/integrations/connect-and-sync-data#connections-for-external-tools)

Connections for external tools

An integration imports business data into cfo.ai. A connected external MCP server or API gives Ari access to another service’s tools. The cfo.ai MCP server does the opposite: it lets an outside AI client use cfo.ai’s tools. These are separate connection types with different setup and access controls.

## 

[​](https://docs.cfo.ai/integrations/connect-and-sync-data#related)

Related

- [Browse the integrations directory](https://docs.cfo.ai/integrations/integrations-directory)
- [Connect the cfo.ai MCP server](https://docs.cfo.ai/integrations/mcp-server)
- [Attach files to a chat message](https://docs.cfo.ai/workspace-settings/file-attachments-in-chat)

Ctrl+I