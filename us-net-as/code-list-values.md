# Code list values

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II, III and IV of the Implementing Rule. To pass this test verify that any instance of an attribute:

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.
* takes only a value explicitly specified in the INSPIRE code list register or shall take a value that is narrower (i.e. more specific) than those explicitly specified in the application schema when the code list‘s extensibility is 'narrower'.
* takes values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'open' or if a value is not one of the values listed in the code list register check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements (This last check is a manual test).


The following check is performed for every feature in the dataset, for the 'open' codelist:

* Check that all the [utilityDeliveryType](#utilityDeliveryType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue). If the check fails a manual check will be required asking to review the code list definition in order to verify that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).

* Check that all the [warningType](#warningType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue1). If the check fails a manual check will be required asking to review the code list definition in order to verify that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).

* Check that all the [utilityNetworkType](#utilityNetworkType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue2). If the check fails a manual check will be required asking to review the code list definition in order to verify that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).


| <a name="preDefinedValue"></a> Pre-defined values for xlink:href attribute of [utilityDeliveryType](#utilityDeliveryType) element are available in the INSPIRE Registry| 
| ---- | 
| UtilityDeliveryTypeValue: http://inspire.ec.europa.eu/codelist/UtilityDeliveryTypeValue | 

| <a name="preDefinedValue1"></a> Pre-defined values for xlink:href attribute of [warningType](#warningType) element are available in the INSPIRE Registry| 
| ---- | 
| WarningTypeValue: http://inspire.ec.europa.eu/codelist/WarningTypeValue | 

| <a name="preDefinedValue1"></a> Pre-defined values for xlink:href attribute of [utilityNetworkType](#utilityNetworkType) element are available in the INSPIRE Registry| 
| ---- | 
| UtilityNetworkTypeValue: http://inspire.ec.europa.eu/codelist/UtilityNetworkTypeValue | 


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Automated + Manual check (if required)

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/> | XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. Please note that the URIs of all code list values from the INSPIRE Registry shall be referenced using the http protocol. 
reviewCodeListValue <a name="reviewCodeListValue"/> | XML document '{filename}', {featureType} '{gmlid}': The property '{property}' has a value '{value}' that is not one of the pre-defined values in the INSPIRE data specification. The same value is used by {count} other features in the dataset, too. Extensions to the pre-defined values are allowed, but must not overlap with one of the pre-defined values and be consistent with the specification of the property. Please review the definition of the value. Please note that the URIs of all code list values from the INSPIRE Registry shall be referenced using the http protocol. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression				|Multiplicity       |Voidable
---------------------------------------------------------- | -------------------------------|-------------------|---------
utilityDeliveryType <a name="utilityDeliveryType"></a> | //schema-element(/us-net-common:Pipe)/us-net-common:utilityDeliveryType/@xlink:href <br> //schema-element(/us-net-common:Duct)/us-net-common:utilityDeliveryType/@xlink:href <br> //schema-element(/us-net-el:ElectricityCable)/us-net-common:utilityDeliveryType/@xlink:href <br> //schema-element(/us-net-ogc:OilGasChemicalsPipe)/us-net-common:utilityDeliveryType/@xlink:href <br> //schema-element(/us-net-sw:SewerPipe)/us-net-common:utilityDeliveryType/@xlink:href <br> //schema-element(/us-net-th:ThermalPipe)/us-net-common:utilityDeliveryType/@xlink:href <br> //schema-element(/us-net-wa:WaterPipe)/us-net-common:utilityDeliveryType/@xlink:href | 0..1 | Yes
warningType <a name="warningType"></a> | //schema-element(/us-net-common:Pipe)/us-net-common:warningType/@xlink:href <br> //schema-element(/us-net-common:Duct)/us-net-common:warningType/@xlink:href <br> //schema-element(/us-net-el:ElectricityCable)/us-net-common:warningType/@xlink:href <br> //schema-element(/us-net-ogc:OilGasChemicalsPipe)/us-net-common:warningType/@xlink:href <br> //schema-element(/us-net-sw:SewerPipe)/us-net-common:warningType/@xlink:href <br> //schema-element(/us-net-th:ThermalPipe)/us-net-common:warningType/@xlink:href <br> //schema-element(/us-net-wa:WaterPipe)/us-net-common:warningType/@xlink:href | 1 | Yes
utilityNetworkType <a name="utilityNetworkType"></a> | //schema-element(/us-net-common:UtilityNetwork)/us-net-common:utilityNetworkType/@xlink:href | 1 | No
