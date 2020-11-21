# Code lists

**Purpose**: Verify that code lists extensions can be accessed.

**Prerequisites**

**Test method**

* Verify that any code list extensions are publicly accessible via HTTP, i.e. inspect extensible code list values property elements. If a reference (@xlink:href) has a value that does not start with http://inspire.ec.europa.eu/codelist/, verify that a HTTP GET request to the URI retrieves a document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following extensible code lists:

* Specific Appurtenance Type: [SpecificAppurtenanceTypeValue](#specificAppurtenanceType) (http://inspire.ec.europa.eu/codelist/SpecificAppurtenanceTypeValue)

* Oil, Gas and Chemicals Product Type: [OilGasChemicalsProductTypeValue](#OilGasChemicalsProductTypeValue) (http://inspire.ec.europa.eu/codelist/OilGasChemicalsProductTypeValue)

* Thermal Appurtenance Type: [ThermalAppurtenanceTypeValue](#appurtenanceType)(http://inspire.ec.europa.eu/codelist/ThermalAppurtenanceTypeValue)

* Thermal Product Type: [ThermalProductTypeValue](#thermalProductType)(http://inspire.ec.europa.eu/codelist/ThermalProductTypeValue)



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
specificAppurtenanceType <a name="specificAppurtenanceType"></a> | //schema-element(us-net-common:Appurtenance)/us-net-common:specificAppurtenanceType/@xlink:href | 0..1 | Yes
OilGasChemicalsProductTypeValue <a name="OilGasChemicalsProductTypeValue"></a> | //schema-element(us-net-ogc:OilGasChemicalsPipe)/us-net-ogc:oilGasChemicalsProductType/@xlink:href | 1..\* | Yes
appurtenanceType <a name="appurtenanceType"></a> | //schema-element(us-net-common:Appurtenance)/us-net-common:appurtenanceType/@xlink:href | 1 | Yes
thermalProductType <a name="thermalProductType"></a> | //schema-element(us-net-th:ThermalPipe)/us-net-th:thermalProductType/@xlink:href | 1 | Yes
