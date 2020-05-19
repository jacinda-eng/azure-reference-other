---
title: Azure Monitor Logs reference - AzureActivity
description: Reference for AzureActivity table in Azure Monitor Logs.
ms.topic: reference
ms.service: azure-monitor
ms.subservice: logs
ms.author: bwren
author: bwren
ms.date: 4/30/2020
---

# AzureActivity

 Entries from the Azure Activity log that provides insight into any subscription-level events that have occurred in Azure.

## Categories

- Azure Resources
- Audit
- Security
## Solutions

- LogManagement
## Resource types

- Analysis Services
- Data Lake Storage Gen1
- Data Lake Analytics
- Power BI Dedicated
- Data Share
- SQL Managed instance
- SQL server
- SQL database
- Azure Database for MySQL server
- Azure Database for PostgreSQL server
- Azure Database for PostgreSQL server
- Azure Database for MariaDB server
- Device Provisioning Services
- Event Hub
- Application Gateway
- Firewall
- ExpressRoute circuit
- Front Door
- Load balancer
- Network interface
- Network security group
- Public IP addresses
- Traffic Manager profile
- Virtual network gateway
- Virtual network
- Search Services
- Stream Analytics
- Bastion
- Recovery Services vault
- Azure API for FHIR
- Data factory (V2)
- API Management services
- Machine learning services
- HDInsight cluster
- Batch account
- CDN profile
- Azure Spring Cloud
- Media Services
- Azure Cache for Redis
- Cognitive Services
- Key vault
- App Service
- Storage account
- SignalR
- Container registry
- Azure Data Explorer cluster
- Azure AD Domain Services
- Azure Blockchain service
- Event Grid domain
- Virtual machine
- Virtual machine scale set
- Kubernetes Services
- Azure Databricks Services
- Azure Monitor autoscale settings
- IoT Hub
- Azure Cosmos DB account
- Machine Learning
- Service Fabric cluster
- Logic App
- Automation account
- Service Bus




## Columns

|Column|Type|Description|
|---|---|---|
|ActivityStatus|string||
|ActivityStatusValue|string|Status of the operation in display-friendly format. Common values include Started In Progress Succeeded Failed Active Resolved.|
|ActivitySubstatus|string||
|ActivitySubstatusValue|string|Substatus of the operation  in display-friendly format. E.g. OK (HTTP Status Code: 200)|
|Authorization|string|Blob of RBAC properties of the event. Usually includes the “action” “role” and “scope” properties. Stored as string. The use of Authorization_d should be preferred going forward|
|Authorization_d|dynamic|Blob of RBAC properties of the event. Usually includes the “action” “role” and “scope” properties. Stored as dynamic column|
|Caller|string|GUID of the caller|
|CallerIpAddress|string|IP address of the user who has performed the operation UPN claim or SPN claim based on availability.|
|Category|string||
|CategoryValue|string|Category of the activity log e.g. Administrative Policy Security|
|Claims|string||
|Claims_d|dynamic||
|CorrelationId|string|Usually a GUID in the string format. Events that share a correlationId belong to the same uber action.|
|EventDataId|string||
|EventSubmissionTimestamp|datetime||
|HTTPRequest|string||
|Level|string|Level of the event. One of the following values: Critical Error Warning Informational and Verbose|
|OperationId|string|GUID of the operation|
|OperationName|string||
|OperationNameValue|string|Identifier of the operation e.g. Microsoft.Storage/storageAccounts/listAccountSas/action|
|Properties|string|Set of <Key Value> pairs (i.e. Dictionary) describing the details of the event. Stored as string. Usage of Properties_d is recommended instead|
|Properties_d|dynamic|Set of <Key Value> pairs (i.e. Dictionary) describing the details of the event. Stored as dynamic column|
|Resource|string||
|ResourceGroup|string|Resrouce group name of the impacted resource.|
|ResourceId|string||
|_ResourceId|string||
|ResourceProvider|string||
|ResourceProviderValue|string|Id of the resource provider for the impacted resource - e.g. Microsoft.Storage|
|SourceSystem|string|Azure is used always for AzureActivity|
|SubscriptionId|string|Subscription ID of the impacted resource.|
|TenantId|string|ID of the worksapce that stores this record|
|TimeGenerated|datetime|Timestamp when the event was generated by the Azure service processing the request corresponding the event.|
|Type|string||