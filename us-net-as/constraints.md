# Constraints [DRAFT]

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

The following checks are performed for every feature in the dataset.

* All utility networks shall have an external object identifier.
* A utility link set must be composed of links and or link sequences that all belong to the same network.
* All utility link sets shall have an external object identifier.
* All utility nodes have an external object identifier.
* The multiplicity of the utilityDeliveryType attribute shall be 0.


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-US](./README.md#ref_TG_DS_US) 5.3.2.2.5.; 5.3.2.2.1.; 5.3.2.2.2.; 5.3.2.2.4.

**Test type**: Automated

**Notes** 

Verify that the OCL constraints that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                  |  XPath expression                                     |Multiplicity       |Voidable
----------------------------- | ----------------------------------------------------- | ------------------|----------
TO BE COMPLETED