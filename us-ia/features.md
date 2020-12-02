# Feature references

**Purpose**: Verify that referenced features can be retrieved.

**Prerequisites**

**Test method**

* Verify that any feature reference in an association role is publicly accessible via HTTP, i.e. inspect all relevant properties. If a reference (@xlink:href) has a value that starts with "#", verify that an element with a `gml:id` attribute with the referenced identifier exists in the same document. If the reference starts with "http", verify that a HTTP GET request to the URI retrieves an XML document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following association role:

* [UtilityNetwork.networks](#networks): UtilityNetwork 
* [Cabinet.nodes](#nodes1): Appurtenance
* [Manhole.nodes](#nodes2): Appurtenance
* [Pole.nodes](#nodes3): Appurtenance
* [Tower.nodes](#nodes4): Appurtenance
* [Duct.cables](#cables): Cable
* [Duct.ducts](#ducts): Duct
* [Duct.pipes](#pipes): Pipe
* [Pipe.cables](#cablesP): Cable
* [Pipe.pipes](#pipesP): Pipe
* [EnvironmentalManagementFacility.parentFacility](#parentFacility): EnvironmentalManagementFacility


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                         |  XPath expression    | Multiplicity    | Voidable
------------------------------------ | ---------------------|-----------------|------------
UtilityNetwork.networks <a name ="networks"></a>	| //schema-element(us-net-common:UtilityNetwork)/us-net-common:networks/@xlink:href | 0..\* | Yes
Cabinet.nodes <a name ="nodes1"></a>	| //schema-element(us-net-common:Cabinet)/us-net-common:nodes/@xlink:href | 0..\* | Yes
Manhole.nodes <a name ="nodes2"></a>	| //schema-element(us-net-common:Manhole)/us-net-common:nodes/@xlink:href | 0..\* | Yes
Pole.nodes <a name ="nodes3"></a>	| //schema-element(us-net-common:Pole)/us-net-common:nodes/@xlink:href | 0..\* | Yes
Tower.nodes <a name ="nodes4"></a>	| //schema-element(us-net-common:Tower)/us-net-common:nodes/@xlink:href | 0..\* | Yes
Duct.cables <a name ="cables"></a>	| //schema-element(us-net-common:Duct)/us-net-common:cables/@xlink:href | 0..\* | Yes
Duct.ducts <a name ="ducts"></a>	| //schema-element(us-net-common:Duct)/us-net-common:ducts/@xlink:href | 0..\* | Yes
Duct.pipes <a name ="pipes"></a>	| //schema-element(us-net-common:Duct)/us-net-common:pipes/@xlink:href | 0..\* | No
Pipe.cables <a name ="cablesP"></a>	| //schema-element(us-net-common:Pipe)/us-net-common:cables/@xlink:href | 0..\* | Yes
Pipe.pipes <a name ="pipesP"></a>	| //schema-element(us-net-common:Pipe)/us-net-common:pipes/@xlink:href | 0..\* | Yes
EnvironmentalManagementFacility.parentFacility <a name ="parentFacility"></a>	| //schema-element(us-emf:EnvironmentalManagementFacility )/us-emf:parentFacility /@xlink:href | 0..\* | Yes
