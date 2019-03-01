---

Copyright:
  years: 2018, 2019
lastupdated: "2019-02-18"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Architecture, Security, and Compliance
{: #architecture-security-compliance}

## Protection Against Unauthorized Access

{{site.data.keyword.messages-for-rabbitmq_full}} use the following methods to protect data in transit or in storage.
- All {{site.data.keyword.messages-for-rabbitmq}} connections use TLS/SSL encryption for data in transit. The current supported version of this encryption is TLS 1.2.
- Access to the Account, Management Console UI, and API is secured via [Identity and Access Management (IAM)](/docs/services/messages-for-rabbitmq?topic=messages-for-rabbitmq-iam).
- Access to the database is secured through the standard access controls provided by the database. These access controls are configured to require valid database-level credentials that are obtainable only through prior access to the database or through our Management Console UI or API.
- All {{site.data.keyword.messages-for-rabbitmq}} storage for persistent messages is provided on block storage volumes encrypted with [{{site.data.keyword.keymanagementserviceshort}}](/docs/services/key-protect?topic=key-protect-about). Bring-your-own-key (BYOK) for encryption is also available through [Key Protect integration](/docs/services/databases-for-postgresql?topic=databases-for-postgresql-key-protect).
- IP Whitelisting - All deployments support whitelisting IP addresses to restrict access to the service.

## Data Resilience

- Backups are included in the service. {{site.data.keyword.messages-for-rabbitmq}} backups reside in [{{site.data.keyword.cos_full_notm}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-about-ibm-cloud-object-storage) and are also [encrypted](/docs/services/cloud-object-storage?topic=cloud-object-storage-security).
- RabbitMQ backups contain only definitions, topology, and metadata. Messages are not stored in backups.
- All {{site.data.keyword.messages-for-rabbitmq}} deployments are configured with replication. Deployments contain a cluster with three nodes where all three nodes are equal peers.
- If you deploy to an [{{site.data.keyword.cloud_notm}} datacenter](/docs/overview?topic=overview-data_center#data_center), your data has multiple copies and each copy resides on a different host. If you deploy to a [{{site.data.keyword.cloud_notm}} Global location](https://www.ibm.com/cloud/data-centers/), the cluster is spread over the region's availability zone locations. If one data member becomes unreachable, your cluster continues to operate normally.


## General Data Protection Regulation (GDPR) 

If you have an account with IBM Cloud, your personal data is held by {{site.data.keyword.cloud_notm}}. The {{site.data.keyword.IBM_notm}} Data Processing Addendum (Addendum) applies to the processing of client's personal data by {{site.data.keyword.IBM_notm}} on behalf of client in order to provide {{site.data.keyword.IBM_notm}} standard services.  
[IBM DPA](https://www.ibm.com/support/customer/zz/en/dpa.html){:new_window}

{{site.data.keyword.messages-for-rabbitmq}} processes limited client Personal Information (PI) in the course of running the service and optimizing the user experience. 

{{site.data.keyword.messages-for-rabbitmq}} provides a [Data Sheet Addendum (DSA)](https://www.ibm.com/software/reports/compatibility/clarity-reports/report/html/softwareReqsForProduct?deliverableId=040987F07A6111E89D57EFEED3CB8BE9){:new_window} with its policies as a Data Processor regarding content and data protection. 

## HIPAA

{{site.data.keyword.messages-for-rabbitmq}} meets the required {{site.data.keyword.IBM_notm}} controls that are commensurate with the Health Insurance Portability and Accountability Act of 1996 (HIPAA) Security and Privacy Rule requirements. These requirements include the appropriate administrative, physical, and technical safeguards required of Business Associates in 45 CFR Part 160 and Subparts A and C of Part 164. HIPAA must be requested at the time of provisioning and requires a representative to sign a Business Associate Addendum (BAA) agreement with {{site.data.keyword.IBM_notm}}.

## Terms

- [The IBM Privacy Policy](https://www.ibm.com/privacy/us/en/)
- [The IBM Cloud Notices and Terms of Use](https://{DomainName}/docs/overview/terms-of-use/notices.html#notices)

