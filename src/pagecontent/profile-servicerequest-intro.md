# CA ServiceRequest Profile
This Service Request Profile is based upon the core FHIR ServiceRequest resource and created to define the minimal set of data required to request for service such as diagnostic investigations, treatments, or operations to be performed.

This profile defines a service request structure that includes core localisation concepts for use as a diagnostic service request in a Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of 0, which means that they may be missing from a resource when it is exchanged between systems.

In this Canadian Baseline ServiceRequest Profile following elements are required:
* status of the order (ServiceRequest.status)
* progression of a business activity (ServiceRequest.intent)
* on whom or what the service is to be performed (ServiceRequest.subject)
* date of the request (ServiceRequest.authoredOn)
* who initiated the request (ServiceRequest.requester)

### Data Absent Reason
In situations where the minimum cardinality of an element or attribute is 1 and information is missing and the Responder knows the precise reason for the absence of data, Responders SHALL send the reason for the missing information using values (such as [NullFlavor](https://www.hl7.org/fhir/extension-iso21090-nullflavor.html)) from the value set where they exist or using the [DataAbsentReason](http://hl7.org/fhir/StructureDefinition/data-absent-reason) extension.

## Must Support Data Elements
Some elements are labeled as MustSupport meaning that implementations that produce or consume resources SHALL provide "support" for the element in some meaningful way (see [Must Support](https://build.fhir.org/ig/scratch-fhir-profiles/CA-Core/general-guidance.html#must-support) definition).

Following elements are marked as Must Support in the Canadian ServiceRequest profile.

**Must Support elements:**
* identifier
* requisition
* status
* intent
* category
* code
* subject
* encounter
* authoredOn
* requester
* performer

## Usage Note
TBD
