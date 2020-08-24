### Introduction

This implementation guide is provided to support the use of FHIR®© in a Canadian context.

This document is a working specification that is expected to be tested and referenced by FHIR®© system producers and implementation guide authors to enable feedback to improve the content of this guide.

As the output of a National Baseline Initiative, this implementation guide provides basic interoperability expectations for human-patient systems in the Canadian space. The goal of this specification is to expose the implementation guide author community and vendor community to a set of profiles that identify the data elements, code systems and value sets that are commonly present across Canada for a given FHIR resource (e.g., patient, medication, etc.) regardless of use case, jurisdiction or implementation.

The Canadian Baseline Profiles are not expected to be implemented "out-of-the-box". They are intended to be a starting point that more specific profiles (driven by jurisdictional, use-case, and project-specific needs) can build derived profiles from. By exposing a minimal and consistent set of expectations across local and jurisdictional guides, we intend to create a more transparent and uniform landscape for the vendor marketplace to begin aligning to.

Existing Canadian and International implementation guides (e.g., Canadian eReferral, Ontario PPR, US Core, IPS, etc.) were used as an initial frame of reference that the Canadian Baseline profiles further relaxed / constrained / extended to make sense in the Canadian context.




### Status

This guide is a **living document** that includes **scratch** notes and profiles that continue to evolve as they undergo a working group review process in the Summer/Fall of 2020 before being exposed to the larger FHIR community for further maturation through feedback and testing.

More context on the profiling, governance and review process can be found on the [**here**](developmentprocess2.html).

For information on where we are at in the working group review follow our progress in the [Infocentral FHIR Implementation Working Group page](https://infocentral.infoway-inforoute.ca/en/collaboration/wg/fhir-implementations)

The [GitHub repository for this CI build be found here](https://github.com/scratch-fhir-profiles/CA-Core).

### Principles

The following principles were applied when creating the profiles:
- *Start with the profiles outlined in the US Core and avoid arbitrary differences* between Canadian and other international implementation guides to:
  - increase the opportunity for Digital Health / mHealth application reuse across North America
  - reduce developer / vendor effort to adapt to Canadian requirements
- *Only impose additional constraints when strictly necessary* making adjustments as they make sense in the Canadian context. Aligning to the CA Baseline should not **prevent** implementors from participating in specific use cases and/or conforming to existing Canadian implementation guides
- *Provide direction* and set minimal expectations on a few common terminologies (e.g., CCDD, PCLOCD, etc.).
- *Focus on what Canadian implementations currently support* not what they "ought to support". Emerging Canadian concepts can be socialized through extensions, examples, and usage notes but should not be constrained by the Baseline as to be prescriptive.
- *Be consistent* and informed by other pan-Canadian standards where possible.


### Base vs. Baseline vs. Core

The international FHIR community is evolving towards further differentiation between the use of Base, Baseline, and Core terminology to categorize implementation guides. At the time that this implementation guide was authored, the following patterns were discerned:

**National Base Implementation Guides** (e.g., Australian Base, Germany Base, Netherlands Base) provide awareness of localized concepts but do not apply cardinality constraints or required binding strengths that enforce conformance to those concepts. In rare cases, cardinality constraints may be applied to elements that have been [sliced](https://www.hl7.org/fhir/profiling.html#slicing) to ensure the presence of sub-elements if a particular slice is used (ex: identifief coding system). Must support flags are not utilized in Base National Profiles.

**National Baseline Implementation Guides** (e.g., Canadian Baseline) provide awareness of localized concepts and apply minimal cardinality constraints and preferred binding strengths only where appropriate and when expected given national context. In some scenarios, more restrictive constraints may be found on elements that have been [sliced](https://www.hl7.org/fhir/profiling.html#slicing) to support meaningful conformance when standard heterogenous concepts are expected (ex: fixed values for specific systems the slice applies to). Must Support flags are utilized to identify elements that are expected to be supported broadly regardless of use case.

**National Core Implementation Guides** (e.g., US Core, UK Core) define a set of conformance requirements that enforce alignment to localized concepts through cardinality constraints, must support flags, and required/extensible binding strengths. Conformance to these profiles is tied to regulatory and/or contractual agreements in order to necessitate adoption to these more prescriptive specifications.

### CA Baseline Profiles

The list of CA Baseline Profiles can be found [**here**](allartifacts.html).

Each profile defines the minimum mandatory elements, extensions and terminology requirements that MUST be present. For each profile, requirements and guidance are given in a simple narrative summary. A formal hierarchical table that presents a logical view of the content in both a differential and snapshot view is also provided along with references to appropriate terminologies and examples.

Guidance, Capability Statements, and other have not yet been reviewed and added.



-----
Contact: [Russ Buchanan](mailto:rbuchanan@gevityinc.com)



----------------------------------------------------------------------
*Everything below this line will be made into a new page called Profile Development Process*

----------------------------------------------------------------------

This section outlines the process and approach that governed how the profiles in this implementation guide were developed and matured.

### Background

Work began on the CA Baseline in January 2019 as a workstream under the Infocentral FHIR Implementations Working Group. The work was undertaken by a grassroots community of Canadian implementation guide authors, implementors, standards experts and vendors to address the problem of siloed Canadian FHIR-based integration project siloes that were leading to FHIR concepts (resources) being adopted & profiled differently in different projects, contexts, and jurisdictions (i.e. Canadian provinces & territories).

#### Problem Statement

A lack of an available national set of Baseline FHIR Profiles will result in applications and source systems needing to ‘start from scratch’ for each jurisdiction that has implemented a particular use case differently, straining developments costs and willingness for vendors to implement further in the Canadian market. It is understood that implementations such as mHealth applications (e.g., Apple Health), CDS Hooks, and other SMART on FHIR applications require a minimum level of consistency in FHIR Profile structure definitions across implementations in order to have widespread adoption and efficacy.

#### Intent
The CA Baseline exposes the implementation guide and vendor community to what concepts can be expected to be supported across jurisdictions today.

Implementation Guide Authors:
When implementation guide authors leverage the profiles as a starting point, constraints like "Must Support" flag and cardinality are inherited and preferred value sets are more likely to used in the derived implementation guide.

Through derivation of profiles, concepts that were common across existing implementations become ubiquitous in future implementations.

Vendors:
Published baseline profiles offer vendors a stepping stone to begin aligning their systems to Canadian concepts. While vendors will still need to configure their systems to additional constraints to support specific implementations and use cases, conforming to the Baseline will offer vendors a head start across all projects. Consistency across jurisdictions will also mean reduced time, money, and effort spent on implementations by not having to start over with each jurisdictions.

#### Boundaries
- The objective of the Canadian Baseline is not use case driven.
- Implementors are not expected to build an application purely against the Canadian Baseline Profiles. Rather, they should be building their software against jurisdiction or project-specific Implementation Guides that are derived from the CA Baseline)
- The Canadian Baseline Profiles are not about driving what implementers need to do but rather what Canadian Implementation Guide authors need to do.
- The Canadian Baseline Profiles need to be the set of requirements that all Canadian Implementation Guides are capable of incorporating into their guides

### Roadmap to Interoperability
The Baseline is not a silver bullet to Interoperability in Canada, but it is a critical stepping stone in reducing the siloes and improving the consistency across the Canadian Landscape.

There is appetite in Canada's standards and governance community to establish a Canadian Core with stricter conformance that would be enforceable through contractual agreements and jurisdictional procurement practices.
While the Canadian Baseline will likely evolve into or offset a large portion of this work, a larger governance structure is needed to accomplish this goal.

The Canadian Baseline can begin encouraging consistency among various Canadian implementation guides in parallel to the efforts to convene jurisdictional governing bodies and stakeholders to come to a consensus on the set of core use cases and contractual obligations.

#### Comparing a Baseline to a Core Implementation Guide
| Category | Baseline | Core |
| What support is needed from jurisdictions? | Public access to jurisdiction’s FHIR Implementation Guides (i.e. so we can see what constraints a jurisdiction’s projects currently have), use of the Canadian Baseline profiles as a starting point for jurisdictional implementation guides | Policy requirements, contract language, or incentives attached to use of the Core profiles, Jurisdictions need to identify and agree on the use cases / workflows supported by the Core profiles |
| Will implementers align to this without financial / jurisdictional / policy incentives? | Yes, minimal constraints with presence in existing implementations is a natural incentive in aligning new implementation guides to the baseline profiles & their minimum expectations | No. Restrictive constraints that require considerable configuration to be compliant can be a stumbling block in adoption to the profiles if incentives/disincentives are not present. |
| Origin | Community, Essentially “here are the constraints that are out there in FHIR implementations right now” | Policy, “These 10 use cases MUST be supported by every digital health product in the province, country” |
| Frequency / strength of constraints (re: both structure definition and business rules / usage notes) | Few strong constraints, only where deemed that any possible use of a concept would do it in the same way | More constraints, Tighter constraints, Each Core profile is designed to support a specific use case, so more constraints can be expected of implementers |

#### Maturing the Baseline
The process to develop and mature the Canadian Baseline Implementation Guide is outlined below.

<br>
<img src="BaselineRoadmap.png" alt="Baseline Maturity Roadmap" width="1200"/>
<br>
<br>

#### Profile Development Process
A profiling workstream and a governance workstream were established under the Infocentral FHIR Implementations Working Group.

The Governance stream developed a guiding document and terms of reference that defined the purpose and scope of the grassroots initiative. The Governance stream also developed the Baseline Maturity Roadmap that guided the review process found below.

The Profiling stream developed a process for review and split the 24 initial profiles (from the US Core profiles) into three substreams: Entity, Medication, and Clinical. These streams were led by Shamil Nizamov, Igor Sirkovich, and Scott Prior respectively.The vast majority of the initial 24 profiles are in-scope, however a small sub-section have been tabled until further notice; the decision was made to prioritize the review (both internal to the Community and externally) of the FHIR Profiles whose R4 Resources had reached a higher maturity level.

- The goal of the substreams was to position community leaders and subject matter experts to participate in profiling efforts related to their expertise and to expedite the profiling activities so they could occur in parallel.
- Substreams met weekly and used the Baseline principles developed in the Guiding Document.
- Profiling review periods and the updates from each of the substream were provided to the larger community on a bi-weekly basis during the profiling update calls.
- Participants on the substream calls varied based on the profile being reviewed, but included regional implementation guide authors, local and regional implementors, vendors, clinicians, and standards/terminology experts.
- Additional feedback was collected from the community via email and the projects Github issue log. Feedback issuers were reminded to participate in the calls that their feedback/suggestion was being reviewed and discussed.
- After agreement on the proposed changes on the call, the changes were tracked on spreadsheets and modifications were made to the specification in branched repositories.
- A change control process was put into place whereby substream leaders posted pull requests to the Github repository which were reviewed and accepted by a volunteer change manager (Russ Buchanan).

#### Review Process
The substreams reviewed proposed profiling changes with participants as part of the development process.

After the substreams completed their "first pass" at the profiles they were published to the Github repository and available through the Continuous Integration Build and Simplifier projects.

An initial due diligence review was identified as a critical process in maturing the profiles prior to being exposed to the larger FHIR community and tested in connectathons.
The review was intended to increase the fidelity of the profiles by comparing the initial draft of Canadian Baseline Profiles to a variety of domains and ‘live’ Canadian FHIR implementations. Non-Canadian, international specifications were also suggested by the Community at this stage, in an attempt to cover as many domains and use cases as possible.

The following domains and "live" implementation guides were identified for the due diligence review:
- Lab (ACCESS Gateway - Patient & Provider Access to Lab Results, Ontario Lab Information System FHIR Specification)
- Pharmacy/Medication (Alberta / Saskatchewan v3 Implementation, PrescribeIT specification, Ontario's Digital Health Drug Repository)
- Immunizations
- Registries (Ontario's Provincial Provider Registry, Ontario's Provincial Client Registry, Saskatchewan / British Columbia Jurisdictional Implementations - In Development)
- Patient Summaries (International Patient Summary)
- eReferral (Ontario's eReferral Specification)
- COVID-19 (LOGICA COVID-19 FHIR Specification)
