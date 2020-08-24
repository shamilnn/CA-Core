### Background
This section outlines the process and approach that governed how the profiles in this implementation guide were developed and matured.

Work began on the CA Baseline in January 2019 as a workstream under the Infocentral FHIR Implementations Working Group. The work was undertaken by a grassroots community of Canadian implementation guide authors, implementors, standards experts and vendors to address the problem of siloed Canadian FHIR-based integration project siloes that were leading to FHIR concepts (resources) being adopted & profiled differently in different projects, contexts, and jurisdictions (i.e. Canadian provinces & territories).

#### Problem Statement

A lack of an available national set of Baseline FHIR Profiles will result in applications and source systems needing to ‘start from scratch’ for each jurisdiction that has implemented a particular use case differently, straining developments costs and willingness for vendors to implement further in the Canadian market. It is understood that implementations such as mHealth applications (e.g., Apple Health), CDS Hooks, and other SMART on FHIR applications require a minimum level of consistency in FHIR Profile structure definitions across implementations in order to have widespread adoption and efficacy.


### Intent
The CA Baseline exposes the implementation guide and vendor community to what concepts can be expected to be supported across jurisdictions today.

Implementation Guide Authors:
When implementation guide authors leverage the profiles as a starting point, constraints like "Must Support" flag and cardinality are inherited and preferred value sets are more likely to used in the derived implementation guide.

Through derivation of profiles, concepts that were common across existing implementations become ubiquitous in future implementations.

Vendors:
Published baseline profiles offer vendors a stepping stone to begin aligning their systems to Canadian concepts. While vendors will still need to configure their systems to additional constraints to support specific implementations and use cases, conforming to the Baseline will offer vendors a head start across all projects. Consistency across jurisdictions will also mean reduced time, money, and effort spent on implementations by not having to start over with each jurisdictions.


### Value Proposition
Implementation guide authors can leverage the Baseline to reduce  able to reference a baseline of what concepts c, will use the Baseline Profiles as a starting point echo those align  what is already validated as in use across Canada today.

By exposing what is in use across Canada today and identifying what  Provides insight into what concepts are in use by existing systems today
A Baseline validates consistency in existing Canadian Implementation Guides AND
Does the majority of the work to identify critical concepts in use for

(e.g., Canadian Baseline) provide awareness of localized concepts and apply minimal cardinality constraints and preferred binding strengths only where appropriate and when expected given national context. In some scenarios, more restrictive constraints may be found on elements that have been [sliced](https://www.hl7.org/fhir/profiling.html#slicing) to support meaningful conformance when standard heterogenous concepts are expected (e.g., Canada Passport Number for patient identifier).

### Boundaries
- The objective of the Canadian Baseline is not use case driven.
- Implementors are not expected to build an application purely against the Canadian Baseline Profiles. Rather, they should be building their software against jurisdiction or project-specific Implementation Guides that are derived from the CA Baseline)
- The Canadian Baseline Profiles are not about driving what implementers need to do but rather what Canadian Implementation Guide authors need to do.
- The Canadian Baseline Profiles need to be the set of requirements that all Canadian Implementation Guides are capable of incorporating into their guides
- .


### Roadmap to Interoperability
The Baseline is not a silver bullet to Interoperability in Canada, but it is a critical stepping stone in reducing the siloes and improving the consistency across the Canadian Landscape.

There is appetite in Canada's standards and governance community to establish a Canadian Core with stricter conformance that would be enforceable through contractual agreements and jurisdictional procurement practices.
While the Canadian Baseline will likely evolve into or offset a large portion of this work, a larger governance structure is needed to accomplish this goal.

The Canadian Baseline can begin encouraging consistency among various Canadian implementation guides in parallel to the efforts to convene jurisdictional governing bodies and stakeholders to come to a consensus on the set of core use cases and contractual obligations.

The process to develop and mature the Canadian Baseline Implementation Guide is outlined below.

#### Maturing the Baseline
<br>
<img src="BaselineRoadmap.png" alt="Baseline Maturity Roadmap" width="400"/>
<br>

#### Comparing a Baseline to a Core Implementation Guide
| Category | Baseline | Core |
|---|---|---|
| What support is needed from jurisdictions? | Public access to jurisdiction’s FHIR Implementation Guides (i.e. so we can see what constraints a jurisdiction’s projects currently have), use of the Canadian Baseline profiles as a starting point for jurisdictional implementation guides | Policy requirements, contract language, or incentives attached to use of the Core profiles, Jurisdictions need to identify and agree on the use cases / workflows supported by the Core profiles |
| Will implementers align to this without financial / jurisdictional / policy incentives? | Yes, minimal constraints with presence in existing implementations is a natural incentive in aligning new implementation guides to the baseline profiles & their minimum expectations | No. Restrictive constraints that require considerable configuration to be compliant can be a stumbling block in adoption to the profiles if incentives/disincentives are not present. |
| Origin | Community, Essentially “here are the constraints that are out there in FHIR implementations right now” | Policy, “These 10 use cases MUST be supported by every digital health product in the province, country” |
| Frequency / strength of constraints (re: both structure definition and business rules / usage notes)|Few strong constraints, only where deemed that any possible use of a concept would do it in the same way | More constraints, Tighter constraints, Each Core profile is designed to support a specific use case, so more constraints can be expected of implementers |


#### Profile Development Process
A profiling workstream and a governance workstream were established under the Infocentral FHIR Implementations Working Group.

The Governance stream developed a guiding document and terms of reference that defined the purpose and scope of the grassroots initiative. The Governance stream also developed the Baseline Maturity Roadmap that guided the review process found below.

The Profiling stream developed a process for review and split the 24 initial profiles (from the US Core profiles) into three substreams: Entity, Medication, and Clinical. These streams were led by Shamil Nizamov, Igor Sirkovich, and Scott Prior respectively.
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
The review was intended to increase the fidelity of the profiles by comparing the initial draft of Canadian Core Profiles to a variety of domains and ‘live’ Canadian FHIR implementations.

The following domains and "live" implementation guides were identified for the due diligence review:
- Lab
- Pharmacy/Medication
- Immunizations
- Registries (Ontario Provincial Provider Registry, Ontario Provincial Client Registry)
- Patient Administration
- Patient Summaries (International Patient Summary)
- eReferral (Ontario eReferral)
- COVID-19 (LOGICA FHIR Spec)
