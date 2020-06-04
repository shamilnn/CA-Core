## Using codes in Observation
Additional codes that translate or map to the Observation code or category codes are allowed (see [CodeableConcept](http://hl7.org/fhir/R4/datatypes.html#CodeableConcept) data type). 
For example: providing both a local code and LOINC code providing a more specific category codes, SNOMED CT concept, or system specific codes.


## Category
The _Observation.category_ specifies a code that classifies the general type of observation being made. The _Observation.category_ element is [CodeableConcept](http://hl7.org/fhir/R4/datatypes.html#CodeableConcept) data type and more than one code is allowed.

For interoperability reason one of the codes SHOULD be from the FHIR standard defined [Observation Category Codes](https://www.hl7.org/fhir/valueset-observation-category.html).

Local codes are allowed as well. In case of using local codes and to better classify the type of observation, both _category.coding.system_ and _category.coding.code_ SHOULD be provided.

## Code
The Observation.code element describes what was observed. Sometimes this is called the observation "name".
FHIR standard recommended pattern is to utilize a LOINC code. For use in a Canadian context the [pan-Canadian LOINC Observation Code Database (pCLOCD)](https://infocentral.infoway-inforoute.ca/en/standards/canadian/pclocd-loinc) is recommended instead.

## value[x] and dataAbsentReason
At its core, Observation uses a name-value pair to code data. However, when the value for the actual observation is not know, i.e., _Observation.value[x]_ is missed, the _Observation.dataAbsentReason_ SHALL be present and provide a reason why the expected value is missing.
Also, the _Observation.dataAbsentReason_ SHALL only be present if _Observation.value[x]_ is not present
