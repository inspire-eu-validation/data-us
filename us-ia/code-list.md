# Code lists

**Purpose**: Verify that code lists extensions can be accessed.

**Prerequisites**

**Test method**

* Verify that any code list extensions are publicly accessible via HTTP, i.e. inspect extensible code list values property elements. If a reference (@xlink:href) has a value that does not start with http://inspire.ec.europa.eu/codelist/, verify that a HTTP GET request to the URI retrieves a document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following empty code lists:

* [SpecificAppurtenanceTypeValue](#SpecificAppurtenanceTypeValue): http://inspire.ec.europa.eu/codelist/SpecificAppurtenanceTypeValue

* [OilGasChemicalsProductTypeValue](#OilGasChemicalsProductTypeValue): http://inspire.ec.europa.eu/codelist/OilGasChemicalsProductTypeValue

* [ThermalAppurtenanceTypeValue](#ThermalAppurtenanceTypeValue): http://inspire.ec.europa.eu/codelist/ThermalAppurtenanceTypeValue

* [ThermalProductTypeValue](#ThermalProductTypeValue): http://inspire.ec.europa.eu/codelist/ThermalProductTypeValue


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression      |Multiplicity   |Voidable
---------------------------------------------------------- | -----------------------|---------------|---------------------------------
SpecificAppurtenanceTypeValue <a name="SpecificAppurtenanceTypeValue"></a> | //schema-element(us-net-common:Appurtenance)/us-net-common:specificAppurtenanceType/@xlink:href | 0..1 | Yes
OilGasChemicalsProductTypeValue <a name="OilGasChemicalsProductTypeValue"></a> | //schema-element(us-net-ogc:OilGasChemicalsPipe)/us-net-ogc:oilGasChemicalsProductType/@xlink:href | 1..\* | Yes
ThermalAppurtenanceTypeValue <a name="ThermalAppurtenanceTypeValue"></a> | //schema-element(us-net-common:Appurtenance)/us-net-common:appurtenanceType/@xlink:href | 1 | Yes
ThermalProductTypeValue <a name="ThermalProductTypeValue"></a> | //schema-element(us-net-th:ThermalPipe)/us-net-th:thermalProductType/@xlink:href | 1 | Yes
