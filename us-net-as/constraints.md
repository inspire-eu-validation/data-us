# Constraints

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

The following checks are performed for every feature in the dataset:

* Check that all [UtilityLinkSets](#UtilityLinkSets) objects have an external object identifier. (OCL:*/inv: inspireId->notEmpty())
* Check that all [UtilityNode](#UtilityNode) objects have an external object identifier. (OCL:*/inv: inspireId->notEmpty())
* Check that the multiplicity of the [utilityDeliveryType](#utilityDeliveryType) attribute is 0. (OCL:*/inv: utilityDeliveryType->size()=0)


The following check shall be manually performed for every feature in the dataset:

* Check that all utility link sets are composed of links and/or link sequences that all belong to the same network.


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-US](./README.md#ref_TG_DS_US) 5.7.2.1.4.; 5.7.2.1.11.; 5.7.2.1.12.; 5.7.2.1.14.

**Test type**: Automated + Manual

**Notes** 

UtilityLinkSets is an abstract utility network class which groups common properties of Cable, Pipe and Duct featureTypes.

The following contraints need to be better verified:
* All utility networks shall have an external object identifier.

Verify that the OCL constraints that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                  |  XPath expression                                     |Multiplicity       |Voidable
----------------------------- | ----------------------------------------------------- | ------------------|----------
UtilityLinkSets objects <a name="UtilityLinkSets"></a> | //schema-element(us-net-el:ElectricityCable)/net:inspireId <br> //schema-element(us-net-common:Pipe)/net:inspireId <br> //schema-element(us-net-ogc:OilGasChemicalsPipe)/net:inspireId <br> //schema-element(us-net-sw:SewerPipe)/net:inspireId <br> //schema-element(us-net-th:ThermalPipe)/net:inspireId <br> //schema-element(us-net-wa:WaterPipe)/net:inspireId <br> //schema-element(us-net-common:Duct)/net:inspireId  | 0..1 | No
UtilityNode objects <a name="UtilityNode"></a> | //schema-element(us-net-common:Appurtenance)/net:inspireId | 0..1 | No
utilityDeliveryType <a name="utilityDeliveryType"></a> | //schema-element(us-net-common:Duct)/us-net-common:utilityDeliveryType | 0..1 | Yes
