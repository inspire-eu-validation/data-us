# Basic test

**Purpose**: Verify that the spatial data set contains at least one Utility and Government Services feature.

**Prerequisites**

**Test method**

* Check that the set of [features](#features) in the spatial data set is not empty. Otherwise report [noFeature](#noFeature)

**Reference(s)**: 

* [TG DS-US](./README.md#ref_TG_DS_US) 5.4, 5.5

**Test type**: Automated

**Notes**

There is no requirement that we could reference in the Technical Guidelines. Maybe such a requirement should be added in the future revision?

## Messages

Identifier  |  Message text (parameters start with '$')
----------- | -------------------------------------------------------------------------
noFeature <a name="noFeature"/>  |  	The XML documents representing the spatial data set do not contain a feature of any of the spatial object types in the 'Utility and Government Services' application schemas. Therefore, the spatial data set cannot conform to this conformance class. If you have expected to find spatial objects from the application schema in the data set, please consult the statistics information to see the spatial object types that have been found.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                          |  XPath expression
----------------------------------------------------- | ------------------------------------------------------------------
features <a name="features"></a> | //schema-element(us-emf:EnvironmentalManagementFacility) \| //schema-element(us-govserv:GovernmentalService) \| //schema-element(us-net-common:Appurtenance) \|//schema-element(us-net-common:Cabinet) \| //schema-element(us-net-common:Duct) \| //schema-element(us-net-common:Manhole) \| //schema-element(us-net-common:Pipe) \| //schema-element(us-net-common:Pole) \| //schema-element(us-net-common:Tower) \| //schema-element(us-net-common:UtilityLink) \| //schema-element(us-net-common:UtilityLinkSequence) \| //schema-element(us-net-common:UtilityNetwork) \| //schema-element(us-net-el:ElectricityCable) \| //schema-element(us-net-ogc:OilGasChemicalsPipe) \| //schema-element(us-net-sw:SewerPipe) \| //schema-element(us-net-th:ThermalPipe) \| //schema-element(us-net-wa:WaterPipe)
