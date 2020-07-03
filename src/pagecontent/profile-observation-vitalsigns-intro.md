# CA Core Observation (Vital Signs) Profile
CA Core uses the Vital Signs profiles from the FHIR Observation resource specification - http://hl7.org/fhir/R4/observation-vitalsigns.html 
The FHIR Vital Signs profile sets minimum expectations for the Observation resource to record, search and fetch the vital signs associated with a patient that include the primary vital signs plus additional measurements such as height, weight and BMI.

## Supported Profiles
CA Core uses other vital signs profiles instantiated from core FHIR Vital Signs:
* BMI - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign body mass index - http://hl7.org/fhir/R4/bmi.html
* BP - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign blood pressure - http://hl7.org/fhir/R4/bp.html
* BodyHeight - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign body height - http://hl7.org/fhir/R4/bodyheight.html
* BodyWeight - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign body weight - http://hl7.org/fhir/R4/bodyweight.html
* BodyTemp - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign body temperature - http://hl7.org/fhir/R4/bodytemp.html
* HeartRate - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign heart rate - http://hl7.org/fhir/R4/heartrate.html
* OxygenSat - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign oxygen saturation - http://hl7.org/fhir/R4/oxygensat.html
* RespRate - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign respiratory rate - http://hl7.org/fhir/R4/resprate.html

## Open Issues
**CA Core Notes:** It is possible to replace some of Vital Signs profiles with CA Core specific. However, what is rational for introducing additional layers of complexity and formality that may be unwelcome, particularly for those systems that do not currently foresee a need to support both FHIR Vital Signs and CA Core Vital Signs profiles.

Feedback is welcome.
