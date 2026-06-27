# azure-exam


security operator role to group can only create and manage security events


vent2 --- vnet1 --- vnet3    (vnet1 can be route to 2 and 3, while 2 and 3 can only be routed to 1)

User Access Administrator role are only related to the specific access of each user to access different Azure resources. This role cannot create or manage any type of Azure resources

– Error, which logs critical failures

– Warning, which highlights potential issues requiring attention

– Information, which logs general app operations

– Verbose provides extensive details for deep debugging

Recovery Services vaults handle comprehensive backup and disaster recovery (Site Recovery) for both Azure and on-premises workloads, while Backup vaults are streamlined, modern storage targets designed exclusively for Azure-native workloads

azure backup can backup a VM even if its switched off. 

availability set ensures if a hardware or software failure happens, only a subset of your VMs are impacted and your overall solution stays operational


ASP stacks
- ASP.NET V4.8 = Windows

- Node 16 LTS = Windows & Linux

- PHP 8.2 = Linux

- Python 3.10 = Linux

- Java 11 = Windows & Linux


standard or premium asp allows for slot creation


Azure custom script is used to bootstrap scripts to Azure VM during creation

Azure Desired State Configuration (DSC) for software installation at vm startup. it provides a high level of consistency and management capabilities than azure custom script


When an error involves 500 and above which is server side, enable webserver logging feature in the appservice

Enable application log for client side or application error

Set the session persistence to Client IP and protocol if a loadbalancer must handle a successive request from a client IP

you can only have one cloud endpoint and one server endpoint to one sync group in a file server system. 


General-purpose v2 accounts: Basic storage account type for blobs, files, queues, and tables. Recommended for most scenarios using Azure Storage. It supports LRS, GRS, RA-GRS, ZRS, GZRS, RA-GZRS replication options.

General-purpose v1 accounts: Legacy account type for blobs, files, queues, and tables. Use general-purpose v2 accounts instead when possible. Supports LRS, GRS, RA-GRS replication options

BlockBlobStorage accounts: Storage accounts with premium performance characteristics for block blobs and append blobs. Recommended for scenarios with high transaction rates, or scenarios that use smaller objects or require consistently low storage latency. Supports LRS, ZRS replication options

FileStorage accounts: Files-only storage accounts with premium performance characteristics. Recommended for enterprise or high-performance scale applications. Supports LRS, ZRS replication options

BlobStorage accounts: Legacy Blob-only storage accounts. Use general-purpose v2 accounts instead when possible. Supports LRS, GRS, RA-GRS replication options

azcopy make is commonly used to create a container or a file share

azcopy is on;ly used for copy jobs. use azcopy make if a creation is required.

Data in an Azure Storage account is always replicated three times in the primary region. Azure Storage offers four options for how your data is replicated:

Locally redundant storage (LRS) copies your data synchronously three times within a single physical location in the primary region. LRS is the least expensive replication option but is not recommended for applications requiring high availability.

Zone-redundant storage (ZRS) copies your data synchronously across three Azure availability zones in the primary region. For applications requiring high availability.

Geo-redundant storage (GRS) copies your data synchronously three times within a single physical location in the primary region using LRS. It then copies your data asynchronously to a single physical location in a secondary region that is hundreds of miles away from the primary region.

Geo-zone-redundant storage (GZRS) copies your data synchronously across three Azure availability zones in the primary region using ZRS. It then copies your data asynchronously to a single physical location in the secondary region.


you cannot enable zone redundancy in gp v1 storage type.

Azure Import/Export service allows data transfer into Azure Blobs.  The Azure Import/Export service only supports export of Azure Blobs.


You can set a maximum of five access policies on a container, table, queue, or share at a time

Point-to-Site (P2S) VPN connection allows you to create a secure connection to your virtual network from an individual client computer

policy-based VPN type as your gateway prevents remote connection. route-based VPN gateway allows remote connection

NSG requires a manual effort to create a security rule for your azure resource. to automate this, use a custom policy definition in order to automate the requirement.

Service chaining and User-Defined Routes (UDRs) allow for precise control over traffic paths by overriding Azure's default routing

Azure Network Watcher provides tools to monitor, diagnose, view metrics, and enable or disable logs for resources in an Azure virtual network. 

IP flow verify in Azure Network Watcher. The main use case of IP flow verify is to determine whether a packet to or from a virtual machine is allowed or denied based on 5-tuple information and not to capture packets from your virtual machines for a period of 3600 seconds or 1 hour.

Azure rdp default rule opens rdp port from 0.0.0.0

inbound NAT rule allows you to forward traffic from a specific port of the front-end IP address to a specific port of a back-end VM. The traffic is then sent to a specific virtual machine. Use this when a specific vm is required. 

load balancing rule  only defines how incoming traffic is distributed to all the instances within the backend pool

Calico network policies are designed for controlling pod-level traffic within Azure Kubernetes Service (AKS) clusters

Only a Global Administrator role can modify user security question 

you are allowed to move subscriptions between management groups.

There are two types of access controls in a conditional access policy:

Grant - enforces grant or block access to resources.

Session - enable limited experiences within specific cloud applications

tags and locks can be applied to subscription, vm and storage account. 

You can attach a resource in one region to a resource group in another region

Microsoft Identity Manager (MIM) is a comprehensive identity management solution for on-premises and hybrid environments

There are a lot of metrics available that you can use to properly monitor your cloud solutions. Here are the relevant metrics for this scenario:

- Backlogged Input Events - Number of input events that are backlogged. A nonzero value for this metric implies that your job can't keep up with the number of incoming events. If this value is slowly increasing or is consistently nonzero, you should scale out your job.

- Input Events - Number of records deserialized from the input events. This count doesn't include incoming events that result in deserialization errors. Stream Analytics can ingest the same events multiple times in scenarios like internal recoveries and self-joins. Don't expect Input Events and Output Events metrics to match if your job has a simple pass-through query.

- Late Input Events - Events that arrived later than the configured tolerance window for late arrivals.

- Early Events - Events whose application time stamp is earlier than their arrival time by more than 5 minutes.

- Out-of-Order Events -Number of events received out of order that were either dropped or given an adjusted time stamp, based on the event ordering policy. This metric can be affected by the configuration of the Out-of-Order Tolerance Window setting. This is also known as "DroppedOrAdjustedEvents" in the Azure Stream Analytics Metrics.

Any backlup job in Azure is region specific

The Azure Network Watcher Agent VM extension is a component that can be installed on Azure virtual machines to enable advanced network monitoring and diagnostic capabilities.

IT Service Management Connector (ITSMC) allows you to connect Azure to a supported IT Service Management (ITSM) product or service

Data Collector Set DCS is a Windows feature primarily used for collecting performance data on local machines

you need to create a Recovery Services vault first before a backup policy 


To delete a RG, delete ball resources that are locked and backed up

backup vault supported data source ; blob, azure disk, postgres and k8s services. Recovery services vault data source. azure sql data protection manager, backup server, backup agent. 




