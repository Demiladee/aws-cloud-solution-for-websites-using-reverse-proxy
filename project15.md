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