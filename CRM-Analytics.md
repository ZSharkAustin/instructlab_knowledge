#### CRM Analytics
As of Spring 24 Release, explore dashboards faster with improved caching, and use your data offline more confidently with exported metadata in Excel. Orchestrate your data jobs more effectively with run details and shared concurrency.

##### Analytics Experience and Visualizations
As of Spring 24 Release, experience more responsive dashboards that load faster with improved caching. Download data to Excel files that include metadata about the export.

**Get Improved Dashboard Performance with Better Caching:** As of Spring 24 Release, your dashboards are now more responsive and load faster with improved caching. Dashboard query results are now cached, increasing performance with fewer calls to the server.

**Download Metadata from Lenses and Widgets:** As of Spring 24 Release, extract detailed insights and user-specific metadata that supports collaboration and informed decision-making through organized export files. With the new export option in CRM Analytics, you can download data from a lens or widget to an Excel file that contains information about the export. The Excel format with metadata can include the name of the user, the date and time of the export, dashboard and widget titles, groups and filters in the query, and the number of records downloaded.

**Embed CRM Analytics Dashboards in LWR Sites (Beta):** As of Spring 24 Release, you can view and interact with CRM Analytics dashboards in your Lightning Web Runtime (LWR) site by adding the CRM Analytics Dashboard component. For example, you can view visualizations of account data alongside their account information.

**Get More Functionality with the New Dashboard Lightning Web Component (Beta):** As of Spring 24 Release, embed your CRM Analytics dashboards in Lightning Experience pages with the new, native CRM Analytics Dashboard Lightning web component. The component works seamlessly in Lightning Experience pages and LWR sites.

**Create More Efficient Queries with Semi-Joins and Anti-Joins (Generally Available):** As of Spring 24 Release, create cleaner queries with better performance and stop worrying about filter item limitations. Generate semi-join or anti-join results from different datasets in a single SAQL query using the `join` statement with a `join_type` specifier.

###### Get Improved Dashboard Performance with Better Caching
As of Spring 24 Release, Your dashboards are now more responsive and load faster with improved caching. Dashboard query results are now cached, increasing performance with fewer calls to the server.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions.

**How:** Improved dashboard caching in the default behavior. If necessary, you can turn it off. From Setup, in the Quick Find box, enter
```
Analytics, and select Settings. Select Disable dashboard query caching.

```

###### Download Metadata from Lenses and Widgets
As of Spring 24 Release, extract detailed insights and user-specific metadata that supports collaboration and informed decision-making through organized export files. With the new export option in CRM Analytics, you can download data from a lens or widget to an Excel file that contains information about the export. The Excel format with metadata can include the name of the user, the date and time of the export, dashboard and widget titles, groups and filters in the query, and the number of records downloaded.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions.

**How:** To access the new export option, select Share on a lens or dashboard widget and then click the Download tab.

###### Embed CRM Analytics Dashboards in LWR Sites (Beta)
As of Spring 24 Release, let your customers view and interact with CRM Analytics dashboards in your Lightning Web Runtime (LWR) site by adding the CRM Analytics Dashboard component. For example, customers can view visualizations of account data alongside their account information.

**Where:** [This change applies to CRM Analytics in LWR sites accessed through Lightning Experience and Salesforce Classic. CRM Analytics](https://help.salesforce.com/s/articleView?id=sf.exp_cloud_basics_glossary.htm&language=en_US) is available in Developer Edition and for an extra cost in Enterprise and Performance editions, and requires an Experience Cloud license. Note: This feature is a Beta Service. Customer may opt to try such Beta Service in its sole discretion. Any use of the Beta Service [is subject to the applicable Beta Services Terms provided at Agreements and Terms.](https://www.salesforce.com/company/legal/agreements/)

**How:** Use the new CRM Analytics Dashboard Lightning web component in your Experience Cloud pages. From the component palette of an object detail page in Experience Builder, drag the dashboard component to the page.

###### Get More Functionality with the New Dashboard Lightning Web Component (Beta)
As of Spring 24 Release, embed your CRM Analytics dashboards in Lightning Experience pages with the new, native CRM Analytics Dashboard Lightning web component. The component works seamlessly in Lightning Experience pages and LWR sites.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions. Note: This feature is a Beta Service. Customer may opt to try such Beta Service in its sole discretion. Any use of the Beta Service [is subject to the applicable Beta Services Terms provided at Agreements and Terms.](https://www.salesforce.com/company/legal/agreements/)

**How:** Open Lightning App Builder for the page you want to edit. Find (Beta) LWC CRM Analytics Dashboard in the component palette and drag it onto the page.

###### Create More Efficient Queries with Semi-Joins and Anti-Joins (Generally Available)
As of Spring 24 Release, Create cleaner queries with better performance and stop worrying about filter item limitations. Generate semi-join or anti-join results from different datasets in a single SAQL query using the `join` statement with a `join_type` specifier.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions.

**How:** Use the CRM Analytics SAQL editor to create your queries. This example uses a semi-join statement to query for accounts with more than 10 opportunities.

This examples uses an anti-join statement to query for accounts with no opportunities.
```
account = load \"accounts\";
opp = load \"opportunities\";
q = join account by (id) anti, opp by (accountId)

```

##### Analytics Data Integration
As of Spring 24 Release, preview your hierarchical data before running your recipe. Allocate your concurrent data prep jobs to meet your orchestration needs. Get information on when each data prep job started and was canceled.

**Visualize Hierarchies and Flatten Transformations with Preview in the Recipe Editor:** As of Spring 24 Release, preview the results of hierarchical data in aggregate nodes and flatten transformations to ensure that you have the correct output before running your recipe. For example, if you’re flattening a role hierarchy to implement row-level security on a dataset, you can preview the results to verify that they’re as expected before proceeding.

**Control Your Data Prep Concurrency Allocation:** As of Spring 24 Release, allocate your dataflow concurrency towards recipe jobs to meet your orchestration needs. For example, instead of being limited to running two dataflows and one recipe at a time, you can share dataflow concurrency towards recipes and run three recipes at the same time.

**Audit Details of Running and Canceled Data Prep Jobs:** As of Spring 24 Release, Enhanced data prep job information provides details for data prep jobs that are running off schedule or why they were canceled. Now you can see when each job started, who started it, and if a job was canceled, who canceled it and when. You can also view the last person who scheduled or unscheduled a recipe or connection in the job scheduler.

**Get More Usage Information in Data Manager:** As of Spring 24 Release, Manage your data limits with more statistics on the Data Manager Usage page. New usage information includes the number of external uploads and the total number of dataflow and recipe runs in a rolling 24-hour period. You can also see the monthly count of rows output by recipes.

**Trigger Recipes to Run When an External Connection Syncs or a CSV Uploads:** As of Spring 24 Release, Set your event-based recipe schedules to run when an external connection syncs or a CSV upload finishes. Instead of being limited to one event for your trigger, you can select multiple events. Create a recipe schedule to run after a local connection syncs and after an external connection syncs, keeping your recipe up to date regardless of the input source.

**Experience Better Recipe Error Messaging and Reliability:** As of Spring 24 Release, Your recipes are now more reliable and easier to troubleshoot. If an issue occurs, the error message helps you identify the problem and resolve issues faster. In addition, if a recipe requires more resources to run successfully, the resources are automatically increased after the first failure and the job is restarted. The need for increased resources is remembered for subsequent runs. Previously, you needed to open a support case to increase a recipe’s resources.

**Append Data Faster with Incremental Uploads (Generally Available):** As of Spring 24 Release, Improve your data upload time when using the external data API by loading CSV files incrementally. By registering data faster, you can bring in more data to your existing datasets without causing the overall run time to grow exponentially.

**Connect to Amazon Athena (Generally Available):** As of Spring 24 Release, Sync Amazon Athena data to Data Manager by creating a remote connection.

**Connect to Databricks (Generally Available):** As of Spring 24 Release, Create a remote connection using the Databricks connector to sync data from Databricks to Data Manager.

###### Visualize Hierarchies and Flatten Transformations with Preview in the Recipe Editor
As of Spring 24 Release, Preview the results of hierarchical data in aggregate nodes and flatten transformations to ensure that you have the correct output before running your recipe. For example, if you’re flattening a role hierarchy to implement row-level security on a dataset, you can preview the results to verify that they’re as expected before proceeding.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions. This change also applies to Salesforce Data Pipelines in Lightning Experience. Salesforce Data Pipelines is available for an extra cost in Enterprise, Performance, and Unlimited editions.

**How:** In the Data Prep recipe, select an aggregate node (1) in the graph to view the preview results (2).

###### Control Your Data Prep Concurrency Allocation
As of Spring 24 Release, Allocate your dataflow concurrency towards recipe jobs to meet your orchestration needs. For example, instead of being limited to running two dataflows and one recipe at a time, you can share dataflow concurrency towards recipes and run three recipes at the same time.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions.

**Who:** Concurrency allocation is available to users with a CRM Analytics Plus license and the CRMA Analytics Plus Admin permission set.

**How:** From Setup, in the Quick Find box, enter Analytics, and select Settings. Select Enable concurrency limit sharing between dataflows and recipes and save. The capacity for individual concurrent dataflow or recipe runs in your org hasn’t changed, but how you use that capacity is now flexible. You can concurrently run three recipes and no dataflows, two recipes and one dataflow, or one recipe and two dataflows. Enabling concurrency limit sharing can affect your scheduled dataflows and recipes if they or other jobs are already using available slots.

###### Audit Details of Running and Canceled Data Prep Jobs
As of Spring 24 Release, Enhanced data prep job information provides details for data prep jobs that are running off schedule or why they were canceled. Now you can see when each job started, who started it, and if a job was canceled, who canceled it and when. You can also view the last person who scheduled or unscheduled a recipe or connection in the job scheduler.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions. This change also applies to Salesforce Data Pipelines in Lightning Experience. Salesforce Data Pipelines is available for an extra cost in Enterprise, Performance, and Unlimited editions.

**How:** In Data Manager, on the Jobs Manager page, click the job ID to view the details. The Started information includes the user and start date and time. If the job was canceled, Cancelled information shows the user who canceled the job with the date and time.

###### Get More Usage Information in Data Manager
As of Spring 24 Release, Manage your data limits with more statistics on the Data Manager Usage page. New usage information includes the number of external uploads and the total number of dataflow and recipe runs in a rolling 24-hour period. You can also see the monthly count of rows output by recipes.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions. This change also applies to Salesforce Data Pipelines in Lightning Experience. Salesforce Data Pipelines is available for an extra cost in Enterprise, Performance, and Unlimited editions.

###### Trigger Recipes to Run When an External Connection Syncs or a CSV Uploads
As of Spring 24 Release, set your event-based recipe schedules to run when an external connection syncs or a CSV upload finishes. Instead of being limited to one event for your trigger, you can select multiple events. Create a recipe schedule to run after a local connection syncs and after an external connection syncs, keeping your recipe up to date regardless of the input source.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions. This change also applies to Salesforce Data Pipelines in Lightning Experience. Salesforce Data Pipelines is available for an extra cost in Enterprise, Performance, and Unlimited editions.

**How:** On the Recipes page in Data Manager, select Schedule from the recipes options menu. Under Schedule Mode, select Event-based. Select one or more options in the Run Schedule After list.

###### Experience Better Recipe Error Messaging and Reliability
As of Spring 24 Release, Your recipes are now more reliable and easier to troubleshoot. If an issue occurs, the error message helps you identify the problem and resolve issues faster. In addition, if a recipe requires more resources to run successfully, the resources are automatically increased after the first failure and the job is restarted. The need for increased resources is remembered for subsequent runs. Previously, you needed to open a support case to increase a recipe’s resources.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions. This change also applies to Salesforce Data Pipelines in Lightning Experience. Salesforce Data Pipelines is available for an extra cost in Enterprise, Performance, and Unlimited editions.

###### Append Data Faster with Incremental Uploads (Generally Available)
As of Spring 24 Release, Improve your data upload time when using the external data API by loading CSV files incrementally. By registering data faster, you can bring in more data to your existing datasets without causing the overall run time to grow exponentially.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions.

**How:** When using the Analytics External Data API to load data, set the mode to incremental.

###### Connect to Amazon Athena (Generally Available)
As of Spring 24 Release, Sync Amazon Athena data to Data Manager by creating a remote connection.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions. This change also applies to Salesforce Data Pipelines in Lightning Experience. Salesforce Data Pipelines is available for an extra cost in Enterprise, Performance, and Unlimited editions.

**How:** Use Data Manager to create an Amazon Athena connection. Add your AWS security credentials to the advanced properties for each connected object.

###### Connect to Databricks (Generally Available)
As of Spring 24 Release, create a remote connection using the Databricks connector to sync data from Databricks to Data Manager.

**Where:** This change applies to CRM Analytics in Lightning Experience and Salesforce Classic. CRM Analytics is available in Developer Edition and for an extra cost in Enterprise, Performance, and Unlimited editions. This change also applies to Salesforce Data Pipelines in Lightning Experience. Salesforce Data Pipelines is available for an extra cost in Enterprise, Performance, and Unlimited editions.

**How:** Use Data Manager to create a Databricks connection. Add the Databricks personal access token, server, HTTPPath, and database values to the advanced properties for each connected object.
