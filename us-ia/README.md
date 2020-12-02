# Conformance class: Information accessibility, Utility and Government Services

Conformance class for the requirements related to the accessibility of referenced information, for example, information stored in registries (code lists, coordinate reference systems).

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Utility and Government Services".

This conformance class is part of the [INSPIRE Data Specification on Utility and Government Services](../README.md).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [Information accessibility](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/information-accessibility) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-US](#ref_TG_DS_US) | [GML application schemas, Utility and Government Services](../us-gml/README.md) | INSPIRE spatial data set encoded in GML, Utility and Government Services features | n/a |

### Notes

The 'Common Utility Network Elements' application schema inherits feature types defined by the Generic Network Model (specified by the Network application schema). The Network application schema defines additional requirements (codelists, contraints, associations) that are not currently verified. A dedicated Conformance Class will be developed at a second stage.
 
## Feature types <a name="feature-types"></a>

The instantiable feature types are:

* Appurtenance
* Cabinet
* Cable
* Duct
* Manhole
* Pipe
* Pole
* Tower
* Utility Link
* Utility Link Sequence
* Utility Network
* ElectricityCable
* OilGasChemicalsPipe
* SewerPipe
* ThermalPipe
* WaterPipe
* EnvironmentalManagementFacility
* GovernmentalService


*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers only to instances of feature types of this application schema, not to any types specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-US <a name="ref_TG_DS_US"></a>   | [INSPIRE Data Specification on Utility and Government Services – Technical Guidelines version 3.0](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_US_v3.0.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-US](#ref_TG_DS_US)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Code lists](./code-list.md)  | ready for review  | A.5.1 |
| [Feature references](./features.md)  | ready for review  | A.1.4 |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gml            | http://www.opengis.net/gml/3.2
us-net-common  | http://inspire.ec.europa.eu/schemas/us-net-common/4.0
us-net-el 	   | http://inspire.ec.europa.eu/schemas/us-net-el/4.0
us-net-ogc 	   | http://inspire.ec.europa.eu/schemas/us-net-ogc/4.0
us-net-sw  	   | http://inspire.ec.europa.eu/schemas/us-net-sw/4.0
us-net-th  	   | http://inspire.ec.europa.eu/schemas/us-net-th/4.0
us-net-wa 	   | http://inspire.ec.europa.eu/schemas/us-net-wa/4.0

The following variables are used to refer to the corresponding Xpath expressions in all test descriptions:

Variable       | Value
-------------- | -------------------------------------------------
$features      | //schema-element(us-emf:EnvironmentalManagementFacility) \| //schema-element(us-govserv:GovernmentalService) \| //schema-element(us-net-common:Appurtenance) \|//schema-element(us-net-common:Cabinet) \| //schema-element(us-net-common:Duct) \| //schema-element(us-net-common:Manhole) \| //schema-element(us-net-common:Pipe) \| //schema-element(us-net-common:Pole) \| //schema-element(us-net-common:Tower) \| //schema-element(us-net-common:UtilityLink) \| //schema-element(us-net-common:UtilityLinkSequence) \| //schema-element(us-net-common:UtilityNetwork) \| //schema-element(us-net-el:ElectricityCable) \| //schema-element(us-net-ogc:OilGasChemicalsPipe) \| //schema-element(us-net-sw:SewerPipe) \| //schema-element(us-net-th:ThermalPipe) \| //schema-element(us-net-wa:WaterPipe)
