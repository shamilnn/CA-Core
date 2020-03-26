<!--- Text entered into this file will appear at the top of the profiles page before the Formal Views of the profile content. -->

This profile was generated from [HL7 StructureDefinition](https://www.hl7.org/fhir/allergyintolerance.profile.json) on 2019-03-28 and constrained during a review of US Core against Canadian sources.

**Note/Question** PrescribeIT does not appear to use a coded allergy.  Is there a coded list for drug related allergies?

Key differences from [USCoreR4 AllergyIntolerance](https://build.fhir.org/ig/HL7/US-Core-R4/StructureDefinition-us-core-allergyintolerance.html):
- AllergyIntolerance.code profiled with code optional text required (similar to how Medication.code is profiled for PrescribeIT)
- AllergyIntolerance.patient reference updated to profile-patient
