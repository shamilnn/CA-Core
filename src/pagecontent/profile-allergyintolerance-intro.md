# CA Core AllergyIntolerance Profile
This profile sets minimum expectations for the AllergyIntolerance resource to record, search and fetch allergies/adverse reactions associated with a patient. It documents the relevant allergies or intolerances (conditions) for a patient, describing the kind of reaction, agent(s) that cause it, criticality and the certainty of the allergy/adverse reaction.

This profile defines core localization concepts for use in the Canadian context.

## Mandatory Data Elements
All elements or attributes within the FHIR specification have cardinality as part of their definition - a minimum number of required appearances and a maximum number of allowable appearances.

Most elements in the FHIR specification have a minimum cardinality of 0, so most elements are not required and subsequently they may be missing from a resource when it is exchanged between systems.

**Required elements in the AllergyIntolerance profile:**
* subject who has the allergy or intolerance (AllergyIntolerance.patient)

## Must Support Data Elements
Some elements are marked as Must Support. This means that implementations generating, receiving, or otherwise using resources with Must Support elements SHALL provide support for those elements in some meaningful way (see [Must Support](https://build.fhir.org/ig/scratch-fhir-profiles/CA-Core/general-guidance.html#cardinality-and-mustsupport-definitions) definition).

The following elements are marked as Must Support in the AllergyIntolerance profile:

**Must Support elements:**
* identifier
* clinical status of the allergy or intolerance (AllergyIntolerance.clinicalStatus)
* verification status (AllergyIntolerance.verificationStatus)
* code of the allergy or intolerance (AllergyIntolerance.code)
* reference to a subject (AllergyIntolerance.patient)
* reaction to the allergy or intolerance (AllergyIntolerance.reaction)
* substance that caused the adverse reaction event (AllergyIntolerance.reaction.substance)
* manifestation of clinical symptoms (AllergyIntolerance.reaction.manifestation)
* severity of the reaction event (AllergyIntolerance.reaction.severity)

## Usage Note
The _AllergyIntolerance_ resource instance use could be clinical decision support applications to generate/display warnings about potentially harmful medications; any intolerance to other agents (e.g. intolerance to soaps, dressings, latex, etc.) more relevant for at the bedside care.
