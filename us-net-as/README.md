# Conformance class: Application schema, Common Utility Network Elements

Conformance class for the requirements associated with the application schema. 

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Utility and Government Services".

This conformance class is part of the [INSPIRE Data Specification on Utility and Government Services](../README.md).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

none

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-US](./README.md#ref_TG_DS_US) | [GML application schemas, Utility and Government Services](../us-gml/README.md) | INSPIRE spatial data set encoded in GML, Utility and Government Services features | n/a |

### Notes

The “Common Utility Networks Elements” application schema inherits the elements defined by the Generic Network Model in the "Networks” application schema. The "Networks” application schema defines additional requirements (codelists, contraints) that are not currently verified. A dedicated Conformance Class will be developed at a second stage.

## Feature types <a name="feature-types"></a>

The instantiable feature types in the application schema are:

*  Utility Network
*  Utility Network Element
*  Utility Link Set
*  Utility Node
*  Utility Node Container
*  Appurtenance
*  Cabinet
*  Cable
*  Duct
*  Manhole
*  Pipe
*  Pole
*  Tower


*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers to instances of feature types of the two application schemas, Electricity Network and Oil-Gas-Chemicals Network , which specialize those specified in this application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-US <a name="ref_TG_DS_US"></a>   | [INSPIRE Data Specification on Utility and Government Services – Technical Guidelines version 3.0](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_US_v3.0.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-US](#ref_TG_DS_US)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Code list values](./code-list-values.md)  | Draft  | A.1.3  |
| [Constraints](./constraints.md)  | Draft  | A.1.7  |


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
us-net-common  | http://inspire.ec.europa.eu/schemas/us-net-common/4.0
base           | http://inspire.ec.europa.eu/schemas/base/3.3
gml            | http://www.opengis.net/gml/3.2
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace
