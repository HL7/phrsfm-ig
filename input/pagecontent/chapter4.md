### Overview and Definition

The PHR-S FM is divided into four sections: Personal Health, Supportive, Record Infrastructure, and Trust
Infrastructure. Functional profiles can be developed which identify various functions from one or more of these
four sections in order to describe a given system, and allows for further characterization of that profile by the
assignment of priorities to each function in the profile (see Figure 1). While the PHR-S FM should contain all
reasonably anticipated PHR-S functions, it is not intended to comprise the entire list of all functions that may
be found in any specific PHR-S. Again, functional profiles will be developed to constrain the functions for an
intended use (see Section 3.6.1). This document defines the PHR-S Functional Model and describes the
general use of profiles and priorities (see Reference Material for examples of stakeholders that might create
profiles).

{% include img.html img="figure1.png" caption="Figure 1: PHR-S Function List Sections" width="70%" %}

As previously mentioned, the PHR-S FM is divided into four main sections: Personal Health, Supportive,
Record Infrastructure, and Trust Infrastructure. Within the main sections are a number of subsections (parent-
child relationships). Each subsection is comprised of a number of individual functions. Functions describe the
behavior of a system in consumer-oriented language and are intended to be recognizable to all key
stakeholders of a PHR-S. Each function contains a Function Name, Function Statement, and Conformance
Criteria (which are “normative” in an ANSI-accredited standard) as well as other associated information such
as Description (which is reference information and is not a normative part of the ANSI-accredited standard).

The numbering of the functions maintains parent-child relationships between the sections and subsections
(e.g., “PH.1.1 Account Holder Profile” is the parent of child “PH.1.1.1 Identify and Maintain a Patient Record”).
In many cases the parent is fully expressed by the children (see Figure 2). In the aggregate, the PHR-S
Functional Model is intended as the superset of functions from which a subset can be derived by a
Stakeholder Community to illustrate what they need in a PHR-S for their setting. Only a subset of this inclusive
set of functions (one or more PHR-S Functional Profiles) will apply to any particular PHR-S implementation.

{% include img.html img="figure2.png" caption="Figure 2. PHR-S Functional Outline" width="70%" %}

There is one type of mandatory inheritance in the PHR-S FM. All criterion listed in a parent function will be
applicable to all the children of that parent function.

### PHR-S Functional Outline

#### The Functions and Their Use

The PHR-S Functional Model can be used to:

* Promote a common understanding of PHR functions upon which developers, vendors, users and
other interested parties can plan and evaluate PHR functions.
* Provide the necessary framework to drive the requirements and applications of next level
standards, such as PHR content, coding, information models, constructs and interoperability for
information portability between sub-systems of a PHR-S and across more than one PHR-S.
* Establish a standards-based method by which each realm (country) can apply these PHR-S
functions to care settings, uses, and priorities.
* Inform those concerned with new, additional, or other use of PHR data and national infrastructure
what functions can be expected in a PHR-S.

#### Personal Health Section Functions

<u>Description of Personal Health section functions:</u> The Personal Health (PH) section functions are the subset of
PHR-S functions that manage information and features related to self-care and provider based care over time.
PH section functions can yield a summary record of an individual’s care, including ad hoc views of the overall
PHR.

<u>Example of a Personal Health section function:</u> A function to ensure that the individual PHR Account Holder’s
demographic information is captured and maintained so that the individual is unambiguously identified.

<u>Actors for Personal Health section functions:</u> As the subject of PHR information, the PHR Account Holder is
the principal user of PH section functions.

#### Personal Health Support Section Functions

<u>Description of Supportive section functions:</u> The Supportive section functions are the subset of PHR-S
functions that assist the PHR Account Holder with administrative and financial requirements. Also included are
PHR-S functions that provide input to systems that perform clinical research, promote public health and seek
to improve the quality and outcome of health care delivered.

<u>Example of a Supportive section function:</u> A function that will electronically query local immunization registries
to ensure that a person is currently registered and determine the person’s immunization status.

<u>Actors for Supportive section functions:</u> The PHR Account Holder is the principal user of Supportive section
functions, but under certain circumstances, health care providers might be expected to perform various
Supportive section functions.

#### Record Infrastructure Section and Trust Infrastructure Section Functions

<u>Description of Record Infrastructure section functions and the Trust Infrastructure section functions:</u> These two
sections are copied from the EHR-S FM R2 since the record and trust requirements of health information
exchange between the personal and clinical settings overlap heavily. They offer functionality that supports the
Personal Health and Supportive section functions. These functions ensure that the PHR-S provides
information privacy and security, interoperates with other information systems (including PHR and EHR
systems), and helps make PHR-S features accessible and easy to use.

<u>Example of a Record Infrastructure section function:</u> A function to ensure that PHR data, such as an
immunization record, can only be viewed and updated after an individual or system authenticates the user’s
identity within the PHR-S.

<u>Actors for Record Infrastructure section and the Trust Infrastructure section functions:</u> These functions are
generally performed transparently by the PHR-S on behalf of (and without intervention of) PHR-S Account
Holders and other users.

### Common Major Concepts Across the Model

#### Consistency in the Conformance Criteria

Within the authoring group, there was an intentional effort to create language consistency in the conformance
criteria. The “Action-Verb” Hierarchy (see 6.4 The Action-Verb Structure) was established to help create
semantic harmony within the conformance criteria so that, for example, if the Personal Health section has a
conformance criterion using the Action-Verb “Update,” that term has the same meaning as in the Supportive
section’s conformance criteria.

The levels in the Hierarchy are granular and have been arranged in a parent-child relationship. For example,
the Hierarchy reveals that the “Capture” of information covers local data entry (“Enter”) and importation of data
from an external source (“Import”). Similarly, under the “Maintain” section of the Hierarchy, the term “Store”
could invoke Action-Verbs listed below it. If the parent term is not used, then the respective verbs in the child
will be cited individually in the criterion. If the term “Manage” is used, all of the applicable Action-Verbs
included in the Hierarchy are encompassed in that criterion. Authors are responsible for determining whether
one or more of the sub-verbs are appropriate for a given function and must write conformance criteria that
constrain the use of the Action-Verb Hierarchy according to the intent of the profile being created.

#### PHR Account Holder Privacy

It is the bias of this Model that consumer privacy rights be protected to the fullest extent possible. However, as
an international model that attempts to describe functionality for many PHR system sub-types (e.g., integrated
PHR/EHR systems, stand-alone PHR systems, or vendor-provided Web-based systems), statements
concerning consumer control over information are frequently tempered by the phrase (with some variations)
“in accordance with user role, organizational policy, or jurisdictional law.” This phrase does not extend license
to institutions to violate individual rights, but acknowledges that legitimate exceptions may exist to the general
rule of PHR Account Holder control over their PHR information. In all cases, the model requires that the
privacy policy of a PHR system be fully transparent to PHR Account Holders, and that a PHR-S has the ability
to capture a PHR Account Holder’s consent on how his or her personal information may be used and
disclosed (see functions in TI.1.8, Patient Privacy and Confidentiality for additional detail.)

#### Functionality versus Implementation

It is important to note that many functions provide the capacity for functionality (e.g., provide for standards-
based interoperability), but do not give implementation details. A function, when implemented, must be
implemented within the context of the entire PHR-S FM. For example, implementation of many functions
throughout the model are expected to conform to the security and audit functions found within TI.1 (Security)
and TI.2 (Auditable Records), and functions performed “by the PHR Account Holder” may be actually
performed by others as delegated by the Account Holder (see TI.1.2, Entity Authorization).

#### Relevant Standards
Relevant Standards include:
* ISO/TR 14292 "Personal health records - definition, scope, context and global variations of use”

#### Consents, Authorizations, and Preferences

Consumers may desire to declare a consent, authorization, or preference differently in the PHR-S context
than in the EHR-S context. The method of handling consents, authorizations, or preferences is not addressed
by the PHR-S FM. Rather, such issues ought to be addressed during implementation. For example, such
functionality could be implemented in a “services-aware” fashion if desired (for example, as a smart-cloud-
type-query). Differences between multiple versions of consents, authorizations, or preferences may be best
adjudicated by humans. The state of the art may not yet be adequate to handle such adjudication
computationally.

#### Scope of Downstream Uses of PHR data

The PHR-S FM currently only envisions privacy, security, and confidentiality measures that extend to the initial
PHR data-exchange recipient and not to (possible) subsequent recipients of the PHR data that might be
passed on by the initial data-exchange recipient.

This PHR-S FM is universal and therefore generic by design. There may be additional constraints in certain
realms or regions. For example, in the US Realm, the management of laboratory results is subject to the
Clinical Laboratory Improvement Amendments (CLIA) federal regulation.

### Type of Profiles

Characterization of a PHR profile based on its attributes:

* **Scope and nature of content** - Some PHR systems do not contain any patient clinical data, but just have consumer health information,
personal health journals, or information about benefits and/or providers.
Of those PHR systems that have clinical information, some are populated by EHRs, some are disease
specific, some include just specific subsets (e.g., laboratory reports), and some are comprehensive.
* **Source of information** - Data in PHR systems may come from the consumer, patient, caregiver, healthcare provider, payer, or all of
these.
* **Custodian of the record** - The person or organization that manages or maintains the physical record. This may be the consumer or
patient, an independent third party, a healthcare provider, an insurance company, or an employer.
* **Data storage** - Data may be stored in a variety of locations, including an Internet-accessible database, a provider’s EHR-S,
the consumer/patient’s home computer, a portable device such as a smart card or thumb drive, or a
privately maintained database.
* **Degree of Interoperability** - PHR system may be stand-alone or be interoperable with other EHRs/PHRs or somewhere in between.
* **Party controlling access to the data** - While consumers or patients always have the right to access their own data, they do not always determine who else may access it. For example, PHRs that are “views into a provider’s EHR” follow the access rules
set up by the provider. In some cases, consumers do have exclusive control.