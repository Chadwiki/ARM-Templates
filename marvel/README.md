# Deploy an elasticsearch #MARVEL cluster


##Deploy

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fwebtoed%2FARM-Templates%2Fmaster%2Fmarvel%2Fazuredeploy.json" target="_blank">
   <img alt="Deploy to Azure" src="http://azuredeploy.net/deploybutton.png"/>
</a>

1. Fill in the mandatory parameters - clustername, client/master/data count, VNET name, public DNS name, a storage account to hold VM image, shield users and password.

2. Fill in other info and click "OK".

## Using the cluster

Simply SSH to the jumpBox, Or access the cluster via LB public IP:9200 with shield crendentials. 
or LBIP:9200/_plugin/kopf

## Parameters

| Name   | Description    |  Default
|:--- |:---|:---|
| dnsName | Unique public dns name where the master node will be exposed | |
| newStorageAccountName | Unique DNS Name for the Storage Account where the Virtual Machine's disks will be placed ||
| adminUserName | User name for the Virtual Machine. ||
| adminPassword | password of the admin user ||
| vmSize | Instance size of the VM worker node ||
| scaleUnit | Number of Data nodes in the cluster ||
| location | This is the location where the availability set will be deployed ||