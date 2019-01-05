***

ITU eTOM+ITIL standard: https://www.itu.int/rec/T-REC-M.3050-200702-I!Sup1/en
Workday Revenue/Billing: https://www.workday.com/en-hk/applications/financial-management/revenue-management.html

https://www.technavio.com/blog/top-18-cloud-billing-services-companies

https://www.redhat.com/en/files/resources/en-rhcf-enterprise-grade-mgmt-tech-detail-INC0277854.pdf

***

Openstack billing: __[Openstack ceilometer](http://superuser.openstack.org/articles/openstack-billing-cloud-kitty/)__

***
### Openstack thoughts

**hardware** <br>

 - compute --> VMs
 - network --> VMWare NXS
 - storage --> vSan

>just a side link on __[vxrail](http://blog.thenetworknerd.com/2018/03/31/a-tale-of-two-vcenters-vxrail-edition/)__

**virtualization layer**<br>
 - _ESX_
 - _VM_ : --> Nova
 - _NXS_ : --> Neutron with __[openstack plugin](https://wiki.openstack.org/wiki/Neutron/VMware_NSX_plugins)__
 - _vSan_ : --> __[Cinder](https://www.openstack.org/assets/presentation-media/HK-Cinder-Driver-ajauch.pptx)__ 


**control plane**
 - _vcentre_
 - _openstack_ __[integrating with vcentre](https://docs.openstack.org/ocata/config-reference/compute/hypervisor-vmware.html)__
 - _vRA_ .... on side note an interesting article on __[vRA and terraforms](https://grantorchard.com/implementation/2017/11/29/tf-provider-for-vra-first-look.html)__

**configuration and management plane :_infra as code_**

 - _terraform_  :https://www.terraform.io/docs/providers/openstack/
 - _vCa_ : vmware cloud assembly .. VMWare's answer to terraforms. here's an __[intro](https://grantorchard.com/tango/introducing-vmware-cloud-automation-services/)__


+---------------------------------------------------------------------------------------+<br>
|  **WHY USE OPENSTACK and not terraform <--> vCentre**                                                              ?    |<br>
+---------------------------------------------------------------------------------------+<br>
>**_`Terraform -> Maps to Openstack Heat!!`_** <br>

***
### Openstack dissected
----------------------------
__[nice map](https://www.openstack.org/assets/software/projectmap/openstack-map.pdf)__

----------------------------

has container and function management - but for the time being we'll ignore this.<br>

For containers we need focus on kubernetes ... relationship w/ OpenShift?
__[openstack <--> openshift](https://blog.openshift.com/openshift-on-openstack-delivering-applications-better-together/)__


