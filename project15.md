### setting up virtual private network (vpc)

- created a vpc - ACS-vpc

![](images/vpc1.png)

- created internet gateway (igw)

- attached the vpc to igw

![](images/IGW2.png)

![](images/IGWVPC2.png)

- created public and private subnets

![](images/publicsubnet3.png)

![](images/privatesubnet33.png)

- created public and private route tables (rtb)

![](images/publicrtb4.png)

![](images/privatertb44.png)

- associated the different rtbs to their respective subnets

![](images/publicsubnettortb5.png)

![](images/privatesubnettortb55.png)

- added public rtb to igw

![](images/editroutesinternetgatewaypublicrtb6.png)

- created nat gateway

- associated an elastic ip with the nat gateway

- added nat gateway to private rtb

![](images/natgatewayelasticip77.png)

![](images/elasticipnatgateway7.png)

![](images/privatertbnatgateway777.png)

- created external application load balancer (extALB), bastion, datalayer, internal ALB and nginx reverse proxy

![](images/ACSbastionALB88.png)

![](images/extALB8.png)

![](images/intALBtonginx8888.png)

![](images/securitygroupfornginxbastion888.png)

![](images/webserverALBaccess88888.png)

- registered a domain name 

- created records of the domain on aws route53

- created a certificate of the domain on aws certificate manager

![](images/awscertificateroute53record9.png)

![](images/awscertificate9.png)

![](images/awscertificateissued9.png)

- created a database via amazon rds

- created efs accesspoints for wordpress and tooling webservers

- created the efs subnet mountpoints for both webservers

![](images/databasecreation10.png)

![](images/efsaccesspoint10.png)

![](images/efssubnetmountpoint10.png)

![](images/efssubnetmountpoint1010.png)

- created rds key via amazon kms but was unable to use it because of the free tier setup

- added the datalayer private subnets to the subnet configuration for the db

![](images/acsrdskey11.png)

![](images/rdssubnetgroup11.png)

- edited configuration files - they are in the conf folder of this repo - to include necessary dns name, etc

- installed amazon efs-utils, ssl, ssl certificate, and edited the conf file for wordpress and tooling sites on apache

![](images/nginxinstallationamazonefsutilsgitclone12.png)

![](images/nginxinstallationrpmbuild12.png)

![](images/nginxinstallationefsutilsinstallmake12.png)

![](images/nginxinstallationchrony12.png)

![](images/nginxinstallationepelrelease12.png)

![](images/nginxinstallationmakerpm12.png)

![](images/nginxinstallationremirepo12.png)

![](images/nginxsetseboolconf12.png)

![](images/nginxinstallationbuildmakerpmlast12.png)

![](images/nginxinstallationsystemctlchrony121.png)

![](images/apacheWSsslinstallation12.png)

![](images/apacheWSsslcertinfo12.png)

![](images/apacheWSviedit112.png)

![](images/apacheWSviedit12.png)

- installed epel-release, remi repo and other dependencies on bastion instance

![](images/bastioninstanceinstallation12.png)

![](images/bastioninstanceinstallation121.png)

![](images/bastioninstanceinstallation1212.png)

![](images/bastioninstance12.png)

- installed amazon efs-utils, epel-release, etc on nginx

![](images/nginxinstallationamazonefsutilsgitclone12.png)

![](images/nginxinstallationrpmbuild12.png)

![](images/nginxinstallationefsutilsinstallmake12.png)

![](images/nginxinstallationchrony12.png)

![](images/nginxinstallationepelrelease12.png)

![](images/nginxinstallationmakerpm12.png)

![](images/nginxinstallationremirepo12.png)

![](images/nginxsetseboolconf12.png)

![](images/nginxinstallationbuildmakerpmlast12.png)

![](images/nginxinstallationsystemctlchrony121.png)

![](images/nginxinstallationsslcert12.png)

![](images/nginxinstallationsslcert1212.png)

![](images/nginxinstallationsslcertlist12.png)

- created internal and external loadbalancers

- set rules for the load balancers

- created images of instances with the different configurations

- created launch templates of the different images

- created target groups of the launch templates

- set some conf rules for reverse proxy (int alb) before launching wordpress

![](images/ALBrules13.png)

![](images/AMItargetgroup13.png)

![](images/AMIwebservers13.png)

![](images/AWSALB13.png)

![](images/AWSALB131.png)

![](images/AWSintALB13.png)

![](images/AWSintALB131.png)

![](images/intALBreverseproxyconfbeforewordpress13.png)

![](images/bastionlaunchtemplate13.png)

![](images/bastionlaunchtemplates13.png)

![](images/bastionlaunchtemplatess13.png)

![](images/nginxlaunchtemplate13.png)

![](images/nginxlaunchtemplates13.png)

![](images/nginxlaunchtemplatess13.png)

![](images/toolinglaunchtemplate13.png)

![](images/toolinglaunchtemplates13.png)

![](images/toolinglaunchtemplatess13.png)

![](images/wordpresslaunchtemplates13.png)

![](images/wordpresslaunchtemplatess13.png)

![](images/wordpresslaunchtemplateafterreverseconf13.png)