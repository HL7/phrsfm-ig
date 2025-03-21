### Introduction (Rererence)

The following is the HL7 EHR Work Group (EHR WG) -approved Conformance Clause for the PHR System
Functional Model (PHR-S FM). As important background on conformance, please note the following:

* This conformance clause defines what it means to conform to the PHR-S FM.
* Conformance to the PHR-S FM is defined for functional profiles. A PHR system (PHR-S) does
not directly conform to the PHR-S FM, rather it conforms to one or more functional profiles.
* Conformance criteria are associated with every function in the PHR-S FM.
* This conformance clause does not specify testing or validation procedures to determine whether
a PHR-S conforms to a functional profile or whether a functional profile conforms to the PHR-S
FM.

The technical and management staff of the U.S. National Institute of Standards and Technology (NIST),
Information Technology Laboratory provided input and support for the development of this conformance
clause.

### Scope and Field of Application <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a>

This conformance clause defines the minimum requirements for functional profiles claiming conformance to
the PHR-S FM. It also identifies how PHR systems achieve conformance to the Functional Model (FM), which
is via the system’s conformance to a particular functional domain profile, multiple functional profiles, or
combination of domain and companion profiles. This clause specifies:

* The purpose, structure, and use of conformance criteria that are to be included in the PHR-S FM
and conforming functional profiles,
* The rules for defining conforming functional profiles of the PHR-S FM,
* The relationship between functional profiles and PHR systems,
* Sample conformance clauses and use case scenarios,
* Guidance on the conformance requirements that a functional profile might levy on PHR systems,
* Guidance on the purpose and use of a PHR system Conformance Statement.

While the conformance requirements for functional profiles can be found in this clause, they necessarily
reference the PHR-S FM and other sources.

This conformance clause does not specify testing or validation procedures to assess a functional profile’s
conformance to the PHR-S FM. It also does not specify testing or validation procedures to determine whether
a PHR system conforms to a functional profile or matches its Conformance Statement.

### Concepts <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a>

#### Functional Profiles

Creating a functional profile is a method for defining subsets of the PHR-S FM. A functional profile is a
specification which uses the Functional Model to indicate which functions are required, desired, or
implemented for certain PHR systems (e.g., systems characterized by their attributes such as source,
custodian, technical approach, or level of functionality) or for other purposes (e.g., systems based on scope or
nature of information such as chronic conditions). See the figure in Section 5.8 for representative examples.

Functional profiles can be created by healthcare community stakeholders with interest in using and/or
providing a functional profile for a PHR system (e.g., Integrated Delivery Network, or an Employer or Payer
system). Functional profiles can represent the functionality required and desired for the level of functionality
and interoperability, or reflect the functionality incorporated in a vendor’s PHR system. Once a functional
profile is defined it can be implemented by PHR systems or it **MAY** trigger the creation of derived functional
profiles. A derived functional profile is a functional profile that is created from an existing functional profile,
inheriting functions from the base (existing) functional profile.

(NOTE: During the process of creating a Functional Profile, it **MAY** be important to understand and
accommodate clinical processes, work flows and/or interaction(s) of healthcare actors. The international
standard ‘ISO 13940 System of Concepts to Support Continuity of Care’ provides an outline of key principles
and processes in the provision of healthcare. We would highly recommend reviewing this standard as part of
your functional profile development work.)

There are two types of functional profiles: the Domain Functional Profile and the Companion Functional Profile.
The Domain Functional Profile is the common type of profile used to describe a PHR system for a specific
community of stakeholders and/or sponsors (such as, diabetes-specific, asthma-specific, EHR-linked or
payer-linked). Also, a Domain Functional Profile of a PHR system can be for use in a selected realm to meet
the rules, regulations and standards applicable for that realm. The Companion Functional Profile is a type of
profile that must be paired with one or more Domain Functional Profiles. The purpose of a Companion
Functional Profile is to add unique features to a PHR System, such as for research, records management and
evidentiary support, usability, or preventative care. For example, many PHR systems for consumers do not
need to support clinical research. For a clinic that is supporting advanced research, the need **MAY** exist for a
PHR system that is capable of all of the expected functions for routine patient self-monitoring activities, but
also has unique features to support additional data collection needs for research reporting and clinical trials.

The Conformance Clause portion of this standard also supports the creation of other (potentially) unique types
of Companion Functional Profiles, whose goal can be to meet the common (or overarching) needs of
regulation-based or realm-specific requirements.

A formal process exists for registering and balloting functional profiles. Functional profiles that are submitted
to the HL7 EHR Work Group with an attestation of conformance to Section 5, Conformance Clause, of the
HL7 PHR-S FM Standard and successfully complete review by the Work Group are designated as “Registered
functional profiles”. Registered functional profiles that undergo formal public scrutiny via the HL7 consensus
process as an Informative EHR Work Group ballot at the Work Group level will be designated as HL7
Informative functional profiles. HL7 Informative functional profiles are eligible to undergo full HL7 membership
ballot via the HL7 consensus process.

#### Conformance Model <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a>

A PHR-S does not conform directly to the PHR-S FM; rather, a PHR-S conforms to a functional profile (i.e., a
subset – more specifically, a tailored subset) of the PHR-S FM. Conformance to the PHR-S FM is defined for
functional profiles. A functional profile conforms either directly to the PHR-S FM or to another conforming
functional profile. Thus, functional profiles claim conformance to the PHR-S FM and PHR systems claim
conformance to one or more conforming functional profiles. A PHR system can also claim conformance to a
domain functional profile, in combination with one of more companion functional profiles. A PHR system
cannot claim conformance solely to a companion functional profile. Figure 3 illustrates this relationship.

{% include img.html img="figure3.png" caption="Figure 3: Conformance Relationships" width="70%" %}

#### Profile Traceability <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a>

Functional profiles allow for added specificity and extensibility to the FM with changes allowed to the base FM
functions and criteria. Section 6 of this chapter defines rules for these changes. It is also required that any
changes and additions be tracked. Two added columns in profiles accomplish this. One column will document
the unique source FM row number for each item in the new profile (or source profile for a derived profile). The
second column will provide codes for the type of changes from the source FM (or source profile). Together,
these two traceability columns will keep track of the origins of the functions or criteria – and whether it is
modified or unchanged from that within the FM or the source profile. This **MAY** be important when questions
arise as to where did it come from, why did you choose or modify it, etc. It can also be helpful to have
traceability back to the FM functions and criteria if and when revisions to a profile or a derived profile are
needed to reflect care setting, regulatory, technology changes – or when a newer version of the FM is offered.

### Normative Language <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a>

The following keywords (i.e., normative verbs) **SHALL** be used to convey conformance requirements.
* **SHALL** – to indicate a mandatory requirement to be followed (implemented) in order to conform.
Synonymous with ‘is required to’.
* **SHALL NOT** – to indicate a prohibited action. Synonymous with ‘prohibited’.
* **SHOULD** - to indicate an optional recommended action, one that is particularly suitable, without
mentioning or excluding others. Synonymous with ‘is permitted and recommended’.
* **MAY** - to indicate an optional, permissible action. Synonymous with ‘is permitted’.

### Conformance Criteria <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a>

#### Introduction

Every function in the PHR-S FM is associated with a set of conformance criteria. These conformance criteria
form the basis for determining whether the function has been implemented.

#### Criteria in the Functional Profile

Functional profiles also have conformance criteria associated with every function in the functional profile. The
functional profile’s criteria are either (1) adapted from the PHR-S FM criteria with care-setting and application
specific information or (2) if no care-setting or application specific criteria are present, inherited directly from
PHR-S FM. Functional profiles **MAY** change PHR-S FM criteria to match the needs and priorities of the
functional profile’s constituency, e.g., by making it more specific, or changing it from ‘may’ or ‘should’ to ‘shall’.
The functional profile **SHALL NOT** be made less restrictive than the PHR-S FM by changing ‘shall’ criteria to
‘may’ or ‘should’ criteria. (A companion functional profile **MAY** be less restrictive that the FM by ignoring ‘shall’
criterion). Functional profiles **MAY** also add additional criteria.

#### ‘Dependent SHALL’ Criteria

Conformance criteria that contain the keyword ‘shall’ and a dependency on situational conditions are called
‘dependent shall’ criteria. The ‘dependent shall’ **SHALL** contain the phrase “according to user role,
organizational policy, and/or jurisdictional law” or other appropriate grammatical tie-in words (e.g., ‘based on’
rather than ‘in accordance’). A ‘dependent shall’ criteria is used to highlight only these (i.e., user role,
organizational policy, and/or jurisdictional law) conditions. A ‘dependent shall’ criterion is a mandatory criterion
for functional profiles and situational for PHR systems. Specifically,

* All functional profiles **SHALL** inherit the criterion, if the function appears in the functional profile.
* A PHR system **SHALL** implement the Dependent **SHALL** criterion only if the criterion is
applicable per the stated dependency in the PHR-S FM. (Note: If the Dependent **SHALL** criterion
is not applicable to the profile but is still desired, the developer of the profile is permitted to
include and implement the criterion.)

#### Referencing Other Criteria or Functions

There is often a link between functions and their criteria with other functions and criteria. For example, a given
function **MAY** depend on another function or on a specific criterion associated with another function.
A criterion in the functional profile that references another function in the functional profile **SHALL** reference
that function by indicating its Function ID and Function Name, as “X.n.n (Name)” (e.g., “PH.1. 5 (Manage
Consents and Authorizations)”. If the referenced function is required to be implemented, then all the ‘shall’
criteria of this referenced function apply. If the referenced function is a parent function that has child functions
(i.e., sub-functions), the reference must be explicit regarding whether the child functions are included in the
reference, all or selected ones. See the examples below:

*  The system SHALL/SHOULD/MAY conform to TI.1.1 (Entity Authorization).
* The system SHALL/SHOULD/MAY conform to TI.2 (Audit) and all child functions.
* The system **SHALL** conform to S.1 Personal Health Support and separate function(s) The system
SHALL conform to S.1 Provider Information. The system **SHALL** conform to S.2 Financial
Management and all child functions.

A criterion in the functional profile that references a specific criterion in another function **SHALL** reference that
function by rewriting the referenced criterion as one of its own and indicating the function and criterion number
from where it came (e.g., F#, CC3).

### PHR-S FM Structure and Extensibility <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a>

#### Hierarchical Structure

Functions **MAY** be contained (i.e., nested) within other functions. A nested function is a ‘child’ to its ‘parent’
(i.e., the function that contains it). A child **SHALL** always have a parent. A function that is not a parent to
another function is considered a ‘leaf’. Figure 4 illustrates this hierarchical structure.
The PHR-S FM is represented as a hierarchical list of functions, consisting of functional parents, functional
header children and functional leaf functions. Headers include an ID, Name and “H” in the column labeled
“Type”. Headers **MAY** contain conformance criteria only if the criteria apply to all its descendent functions
(children, grandchildren, etc.). All parent functions **SHALL** be designated as a header (“H”) function. Leaf
functions contain at a minimum the following: ID, Name, Statement, Description, and Conformance Criteria
and have an “F” in the “Type” column.

Conformance criteria listed in a header function **SHALL** be inherited by all its children functions. Similarly,
conformance criteria listed in a parent function **SHALL** be inherited by all its children functions. Conformance
Criteria have a “C” in the “Type” column.

{% include img.html img="figure4.png" caption="Figure 4: Portion of the Functional Model hierarchical structure" width="70%" %}

(Note: The numbering schema above reflects functions in the Personal Health section. For instance, PH.1.1 is
the function ‘Identify and Maintain a PHR Account Holder Record.)

Functional profiles either:
* Select functions from the PHR-S FM for inclusion in the functional profile,
* Deem a function in the PHR-S FM as not applicable, thus do not select it for inclusion in the
functional profile,
* Add a new child function when it has been determined that there is no applicable function in the
PHR-S FM to represent a functional need in the functional profile.

#### Naming Convention

Functional profiles **SHALL NOT** change the name or statement of a function except to allow for alignment to
realm specific nomenclature, including language distinctions and implication of non-english translations. In
these cases, the International Organization for Standardization (ISO) country code (ISO 3166 Country Codes)
**SHALL** be appended to the function ID in the functional profile. It is recommended that the HL7 Affiliate for the
respective realm coordinate with the profile development process to maintain a mapping of the Functional
Model function name and/or statement and the realm-adjusted name and/or statement.

#### Priorities

Functional profiles indicate the importance and/or immediacy of a functional profile by associating a priority
with a function. Three priorities have been defined: Essential Now, Essential Future, and Optional.

* Essential Now indicates that the implementation of the function is mandatory, as of the profile
issuance date.
* Essential Future indicates that the implementation of the function is currently optional but will be
mandatory at some future time, which is specified by the functional profile.
* Optional indicates that the implementation of the function is optional.

Any or all of these priorities **SHALL** be used in a functional profile. If the Essential Future priority is used, then
functional profiles are required to define the timeframe associated with implementing functions. A timeframe
MAY be a date, time allotment (e.g., year 2014, or four months after functional profile publication), or event
(e.g., subsequent publication of this functional profile). A functional profile **MAY** define multiple timeframes for
the Essential Future priority. If multiple timeframes are defined, then the timeframe **SHALL** be used to qualify
each occurrence of the Essential Future priority (e.g., EF-2015, EF-2016).

#### Extensibility

To accommodate changes in technology as well as functional profiles’ needs, the PHR-S FM is designed for
extensibility with respect to functions and their related criteria. Incorporation of additional functions in the
functional profile beyond what is defined in the PHR-S FM is accommodated through a set of rules for adding
new functions as defined in Section 5.7.3.

Incorporation of additional criterion, changing the sequence of criterion and providing greater profile-specific
detail, beyond what is defined in the FM, is accommodated through a set of rules for adding new criterion or
changing existing criterion as defined in Section 5.5.2.

### Functional Profile Conformance <a href="https://hl7.org/fhir/versions.html#std-process" title="Normative Content" class="normative-flag">N</a>

#### Introduction

A functional profile claiming conformance to the PHR-S FM **SHALL** meet all requirements specified in section
5.7.2 Rules for Domain Functional Profiles or 5.7.6 Rules for Companion Functional Profiles.

#### Rules for Domain Functional Profiles

Domain functional profiles that adhere to the Rules for Functional profiles **MAY** claim conformance to the
version of the PHR-S FM from which it was derived.
Functional profiles claiming PHR-S FM conformance **SHALL**:

1. Identify the PHR-S FM with version/date from which the functional profile is derived,
2. Include a description, version and issuance date of the functional profile,
3. Contain a conformance clause which
    * a. Defines the requirements that PHR systems must satisfy in order to claim conformance to the
    functional profile.
    * b. Defines the requirements that functional profiles derived from the functional profile (i.e.,
    derived functional profiles) must satisfy in order to claim conformance to the functional profile.
    * c. Specifies that functions designated with the priority ‘Essential Now’ **SHALL** be implemented
    by conformant PHR systems.
    * d. Specifies that functions designated with the priority ‘Essential Now’ **SHALL** be included in any
    derived functional profiles.
    * e. If Essential Future is used, defines the meaning of ‘Essential Future’, including specifying the
    timeframe for when these functions are required to be implemented.
    * f. Requires that at least one function, regardless of its priority, be implemented in order for a
    PHR system to claim conformance to the profile.
4. Identify functions from the PHR-S FM that are applicable to the functional profile. For each function,
indicate its priority (i.e., Essential Now, Essential Future or Optional).
5. For each function, derive conformance criteria based on the PHR-S FM’s conformance criteria.
    * a. In the functional profile, there **SHALL** be at least one criterion for each function that is
    mandatory (a ’shall’ criterion).
    * b. If there are ‘shall’ criteria (for the function in the PHR-S FM), then those criteria **SHALL** also
    exist for the function (in the functional profile). Additionally, if the function is split (in the
    functional profile), then the parent's ‘shall’ criteria **SHALL** appear in at least one child of that
    function.
    * c. If, as yet there is no ‘shall’ criterion (for the function in the PHR-S FM), then at least one of the
    ‘should’ or ‘may’ criterion **SHALL** be made mandatory, i.e., a ‘shall’ criterion.
    * d. Adhere to the rules for referencing functions or criteria in Section 5.5.4.
6. For any function in the PHR-S FM where one or more criteria are ‘dependent shall’ criteria, the
functional profile for that function **SHALL**
    * a. Replicate verbatim each ‘dependent shall’ in the functional profile, regardless of whether the
    dependent situation applies or not.
    * b. When the dependent situation applies, create ‘shall’ criteria that apply the dependency to the
    ‘dependent shall’ criterion, resulting in one or more new, constrained versions of the
    ‘dependent shall’ criterion.
    * c. State the specific scope of practice, organizational policy, and/or jurisdictional law which
    applies or state why these dependencies do not apply.
7. Adhere to the rules for creating new functions in functional profiles in Section 5.7.3.
8. Be structured in accordance with the structural requirements defined for the PHR-S FM in Section 5.6.
9. Complete the two traceability columns, see Section 5.3.3, for any changes to functions or criteria, and
include the following codes for type of change: (1 – sequence, 2 – optionality, 3 – content, 4 – new).
Multiple codes are allowed to document the type of changes. For example, criterion #3 that is moved
to #1, changed from **SHOULD** to SHALL, and with realm specifics on standards required would be
coded as “1, 2, 3”.
10. Be structured in accordance with the structural requirements defined for the FM in Section 5.6.1
11. Use the Glossary Action-Verbs for modifying or creating new conformance criterion.

Functional domain profiles claiming conformance to the PHR-S FM **MAY**:

1. Create additional functions according to the rules specified in Section 5.7.3.
2. Contain conformance criteria more specific and limited in scope than those of the PHR-S FM.
3. Replace the text ‘standard(s)-based’ found in some criteria with specific standards and/or
specifications named at the most discrete level of designation.
4. Change a ‘should’ criterion to a ‘shall’ or a ‘may’ criterion.
5. Change a ‘may’ criterion to a ‘shall’ or a ‘should’ criterion.
6. Ignore a ‘should’ or ‘may’ criterion in the PHR-S FM (i.e., not include it in the functional profile).
7. Add additional conformance criteria beyond those in the PHR-S FM.
8. Make the order of the conformance criteria significant (e.g., put all ‘shall’ criteria first).
9. Enforce common resolution of ambiguous semantics of the PHR-S FM.
10. Make the functional profile public (e.g., published on a web site) so interested parties can see/use it.
11. Submit the functional profile for registration review by the HL7 EHR Work Group.

Functional domain profiles claiming conformance to the PHR-S FM **SHALL NOT**:

1. Specify any requirements that would contradict or cause non-conformance to the PHR-S FM.
2. Modify the name or statement of any function in the PHR-S FM, except to allow for alignment with
realm specific nomenclature as specified in Section 5.6.2.
3. Change a mandatory conformance criteria to an optional criteria (i.e., replace the ‘shall’ within the
criteria to ‘should’ or ‘may’) of any function in the PHR-S FM.
4. Modify any requirements of a function not selected for the functional profile (i.e., all unselected
functions default to the PHR-S FM’s criteria. If a profiling group wants to change something, they
**SHALL** promote it into their functional profile).

#### Rules for Creating New Functions in Functional Profiles

If a function is not adequately specified for a functional profile or does not exist, the functional profile **SHALL**
only create new children; the new children can be parents or leaves. Figure 5 illustrates the addition of a new
child function.

{% include img.html img="figure5.png" caption="Figure 5: Creating a new function" width="70%" %}

The following rules specify the method for creating new functions:

1. Whenever possible, conformance criteria **SHOULD** be used to avoid creating a new function. This
may be done, for example, in cases where the original function’s conformance criteria are too broad:
divide the PHR-S FM’s or base functional profile’s inherited conformance criteria into two criteria in
the functional profile, one being mandatory and the other optional. If this is not possible, the creation
of a new child function and associated criteria is allowed if necessary to clearly define the profile
requirements.
2. When a ‘leaf’ function exists but is too broadly specified in the PHR-S FM or base functional profile
for conformance criteria to adequately constrain it, then the function **MAY** be split as follows:
    * a. The original ‘leaf’ function is retained as the parent of its newly created children functions,
    * b. The original ‘leaf’ function’s conformance criteria **SHALL** be distributed among its children
    functions.
3. When no candidate function exists to express the requirements of a functional profile, a new child
function **MAY** be created (e.g., adding a new kind of summary list under the summary list’s parent).
Parent functions **SHALL NOT** be split. This preserves the structure of the underlying PHR-S FM in the
functional profiles

{% include img.html img="figure6.png" caption="Figure 6: Splitting a function" width="70%" %}

If new children functions are created by a functional profile that is balloted or registered, these new functions
will be captured by the HL7 EHR Work Group and tracked for review. The EHR Work Group **WILL** use these
new functions and related criterion as input and candidates for changes to the FM (e.g., inclusion, relaxation
of conformance criteria). The EHR Work Group **MAY** maintain a file of functions and criterion reviewed and
rejected for inclusion in a future version of the FM.

{% include img.html img="figure7.png" caption="Figure 7: Adding a new child function" width="70%" %}

#### Rules for Derived Functional Profiles

Derived functional profiles claiming conformance to one or more base functional profiles **SHALL**:

1. Adhere to all the rules for functional profiles as specified in Section 5.7.2.
2. Adhere to the rules for creating new functions as specified in Section 5.7.3, if not prohibited by the
base functional profile.
3. Identify the base functional profiles from which it is derived.
4. For each function inherited from a base functional profile, retain and not change mandatory
conformance criteria to optional conformance criteria.

#### Conformance Statement

Functional profiles **MAY** want to require that a conformance statement be produced for systems claiming
conformance to the profile. A Conformance Statement provides information about a PHR system, by
presenting in a uniform manner the functions that have been implemented by the PHR system. A blank (i.e.,
yet to be completed) Conformance Statement typically takes the form of a questionnaire or checklist, to be
completed for each PHR system.

A Conformance Statement provides a concise summary of a functional profile. It follows a standard layout,
thus providing PHR system vendors and users a quick overview of the functional profile’s functions. Moreover,
it can also be used to highlight optional functions and capabilities supported by the PHR systems as well as
document any extensions (i.e., additional functionality beyond what is in the functional profile) or
specializations that have been made. A PHR system’s Conformance Statement provides information that can
be used in assessing the PHR system’s conformance to a specific functional profile. Additionally,
organizations wishing to acquire a PHR system **MAY** produce a Conformance Statement to indicate the
functions that are required and/or desired in a PHR system.

Functional profiles **MAY** want to include a blank Conformance Statement in order to promote consistency
among completed Conformance Statements. Conformance Statements can be useful in determining the
chances of interoperability between two PHR systems, by comparing the functions supported by each PHR
system. Additionally, for conformance testing purposes, it can be used to facilitate the selection of tests that
would be applicable to a particular PHR system being tested. For example, if a PHR system did not implement
functions designated as ‘Essential Future’, this would be evident in the Conformance Statement and the tests
for these functions (which are unimplemented) would not be performed.

#### Rules for Companion Functional Profiles

Companion functional profiles that adhere to the Rules for Functional profiles **SHALL** claim conformance to
the version of the PHR-S FM from which it was derived. Companion functional profiles will follow the section
5.7.2 Rules for Domain Functional Profiles and the section 5.7.4 Rules for Derived Functional Profiles, except
for the exceptions and addition described below:

Companion functional profiles claiming FM conformance **SHALL**:

1. Adhere to section 5.7.3 for adding new functions,
2. Contain a conformance clause which
    * Defines at least one domain functional profile for which the companion functional profile can
    be linked that PHR systems must satisfy in order to claim conformance, or state any specific
    domain functional profiles that can or cannot be linked to the companion functional profile,
    * Defines the requirement(s) that companion functional profiles derived from the base
    companion functional profile (i.e., derived functional profiles) must satisfy in order to claim
    conformance to the companion functional profile.
3. Include **only functions being modified** from the Overarching section of Annex E as Essential
Now and identify functions from other sections of Annex E of the FM that are applicable to the
companion functional profile. For each identified function, indicate its priority (i.e., Essential Now,
Essential Future, or Optional).
4. For each function, derive conformance criteria based on the FM’s conformance criteria.
    * In the functional profile, there **SHALL** be at least one criterion for each function that is
    mandatory (a ’shall’ criterion).
    * If there are ‘shall’ criteria (for the function in the FM), then those criteria **MAY** also exist for
    the function (in the companion functional profile) that it changes. Additionally, if the function
    is split (in the functional profile), then the parent's ‘shall’ criteria **MAY** appear in at least one
    child of that function.
5. For any function in the FM where one or more criteria are ‘dependent shall’ criteria, the
companion functional profile **MAY** elect to ignore the criterion, but if selected for that function
SHALL follow the rules for "Functional profiles claiming PHR-S FM conformance SHALL" list in
section 5.7.2.

Companion functional profiles claiming conformance to the FM **MAY**:

1. Ignore a ‘shall’, ‘‘should’ or ‘may’ criterion in the FM (i.e., not include it in the functional profile).
There are no exceptions to section 5.7.4 for Derived Companion Functional Profiles

### Use Cases and Samples (Reference)

#### Functional Profile Use Cases

##### Example 1: PHR Source (based on custodian)

It is determined that a new source-based functional profile is needed to reflect the specific
requirements and expectation of a system from this particular stakeholder source (e.g., a hospital,
medical group, payer, or health record bank) – see Figure 9. To help ensure widespread use and
uniformity, the functional profile authors elect to undergo the registration review followed by the HL7
consensus process (i.e., submitting the registered functional profile for an “Informative” committee
level ballot). If successful, the result will be designated an HL7 Informative Functional Profile.

After looking at current list of HL7 PHR informative functional profiles, the decision to create a new
functional profile is made. Each function in the PHR-S FM is examined and those that are relevant to
the PHR source chosen – e.g., a Provider-Linked PHR from an Integrated Delivery Network. From
these functions, a small set of ‘core’ functions is selected as being essential and mandatory. For each
function, conformance criteria are developed either adapting the PHR-S FM conformance criteria or in
a few cases, using the PHR-S FM criteria as is. To complete the functional profile, a description of the
functional profile is written that includes its intended use and audience, as well as a conformance
clause. The functional profile is made public by publishing it on various web sites. Additionally, the
functional profile is submitted to HL7’s EHR WG for registration review, comment and ballot.

##### Example 2: Level of Functionality derived functional profile

A Community of Interest (e.g., a regional health information exchange network, or a care
management community who targets a specific chronic condition) or a particular stakeholder may
want a functional profile. The Community of Interest or stakeholder **MAY** want a profile based on the
level of functionality that they want for their patient population, to reflect the expectation of the PHR
system’s sophistication and/or capabilities – see Figure 8.

The Community of Interest or stakeholder does not want to create a new functional profile from
scratch. After looking at the list of HL7 Registered PHR Functional Profiles, they find an existing
functional profile that is very close to what they want. Using this functional profile as the base, they
accept all the functions designated as ‘Essential Now’, reject functions designated as ‘Future’ and add
several more functions. For each function, they review the conformance criteria and adapt the criteria
to reflect their situational information.

##### Example 3: Vendor functional profile

A vendor of a PHR system wants to claim conformance to the PHR-S FM.

The vendor identifies and lists all the functions that are in his product. The vendor adds a description
and a conformance clause (see samples in section 5.8.2). This is the vendor’s functional profile. If the
vendor has actually implemented all the functions listed, then this is equivalent to ‘Essential Now’ and
these functions are mandatory. Vendor features that are not in the PHR-S FM **MAY** be added as
added functions or added criteria – within the rules of sections 5.7.2 and 5.7.3 above. If functions that
are currently implemented and those that will be implemented in the future are listed, then the
functional profile is comprised of ‘Essential Now’ and ‘Essential Future’ and/or optional functionality.
Finally, the vendor adds conformance criteria for each function inheriting directly (without change) the
criteria in the PHR-S FM. This is appealing in that, the vendor has the opportunity to list the current
functionality and, if desired, indicate future plans. In essence, this is similar to a vendor Conformance
Statement (a concept with which most vendors are already familiar). A vendor **MAY** create multiple
functional profiles.

**Figure 8: Examples of Functional Profile Options by "Model" and/or Level of Functionality**

#### Sample Domain Functional Profile Conformance Clauses

##### Developing a Conformance Clause

To aid functional profile developers in developing a conformance clause for their domain functional profile,
as required by Section 5.7.2 rule #3, the following fictional examples are offered. Note: in these examples,
the keywords **‘SHALL’**, **‘SHOULD’**, and **‘MAY’** are capitalized and bold. This is a convention to draw
attention to the keywords.

##### Sample 1: conformance clause for a Provider-linked PHR functional profile

This domain functional profile defines the conformance requirements for PHR systems and derived
functional profiles. To conform to this functional profile, all ‘Essential Now’ functions **SHALL** be
implemented. ‘Essential Now’ functions are considered mandatory functions. A PHR system is conforming
if it implements all the functions designated as ‘Essential Now’ and the mandatory conformance criteria
associated to that function. A derived functional profile is conforming if it follows the Rules for functional
profiles.

Mandatory conformance criteria are indicated by the keyword ‘shall’. Optional conformance criteria are
indicated by the keywords ‘should’ or ‘may’.

PHR systems **SHALL** provide a Conformance Statement structured according to the rules and policies
defined in this functional profile.

##### Sample 2: conformance clause for a vendor system functional profile

Conformance is defined for My-PHRsystem. All functions in this functional profile are mandatory, are
deemed as ‘essential now’, and **SHALL** be implemented in order to conform to this functional profile.

##### Sample 3: conformance clause for a Community of Interest functional profile

Conformance is defined for BuyMyDiabetesPHR. To conform to this functional profile, all functions labeled
as ‘essential now’ **SHALL** be available and have been implemented. Functions labeled ‘essential future’
are optional, in that they are present for informational purposes only and **MAY** be implemented in future
functional profiles.

### Interpreting and Applying Conditional ‘SHALL’ (Reference)

#### Construction of Conformance Criteria Using the Conditional 'SHALL' Overview

Conformance criteria in the FM and those created can be structured in the simple format an Actor followed by
normative verb followed by action or property. For example: The system **SHALL** capture demographic
information as part of the patient record.

However, there are two conditional forms for which if the condition is true, then the following text must apply.
One is If/Then. If condition, then Actor followed by normative verb followed by action. If the condition is not
met (i.e., false) then ignore the rest of the sentence. For example, IF data is exchanged with internal or
external systems, THEN the system **SHALL** conform to function TI.5.4 (Interchange Standards).

The other is a ‘Dependent Shall’ format. Actor followed by normative verb followed by action/interaction
followed by ‘according to scope of practice, organizational policy or jurisdictional law’. For example, “The
system **SHALL** enable EHR-S security administrators to grant authorizations to principals according to scope
of practice, organizational policy, or jurisdictional law.”
The following example of a PHR-S FM ‘dependent shall’ criterion will be used to illustrate concepts throughout
this section.

> PHR-S FM criterion: The PHR-S **SHALL** provide the ability for PHR-S security administrators to grant
authorizations to principals according to user role, organizational policy, and/or jurisdictional law.

#### General Concepts

The purpose of the ‘dependent shall’ is to allow functional profiles to constrain a PHR-S FM ‘shall’ criteria
based on situational conditions such as policy and legal implications. Specifically, the ‘dependent shall’ criteria
in the PHR-S FM are ‘shall’ criteria plus a dependency, where the dependency is defined by:

* <u>User role</u> which applies to the various PHR Account Holder’s possible or alternative roles – which
may be care setting specific or not, or **MAY** be related to whether the PHR is about them or is for
their dependent.
* <u>Organizational policy</u> which refers to a plan or course of action intended to influence and
determine decisions, actions, and other matters of a group of persons organized for a particular
purpose within an association and structure through which individuals cooperate systematically to
conduct business.
* <u>Jurisdictional law</u> which refers to the territorial range of authority or control with the power, right,
or authority to interpret, apply, and declare the body of rules and principles governing the affairs
of a community and enforced by a political authority; a legal system.

The structure of the ‘dependent shall’ criteria in the PHR-S FM is the same as the ‘shall’ criteria except with
the addition of the phrase “according to user role, organizational policy and/or jurisdictional law” or other
appropriate grammatical tie-in words (e.g., “based on” rather than “according to”). Note that all three
dependencies are present in the PHR-S FM ‘dependent shall’ criteria. It is the functional profile that narrows it
to any one dependency or any combination of the three. Moreover, in the functional profile, the specific user
role, organizational policy, and/or jurisdictional law which necessitates evoking the ‘dependent shall’ is
explicitly identified.

> For example: (derived from the PHR-S FM criterion above)

> PHR-S FM criterion: <u>The PHR-S **SHALL** provide the ability for PHR-S security administrators
to grant authorizations in accordance with the U.S. Health Insurance Portability and
Accountability Act of 1996.</u>

The difference between a ‘shall’ criterion and a ‘dependent shall’ criterion is shown in the table below.

| | ‘SHALL’ Criterion | ‘Dependent SHALL’ Criterion |
|---|---|---|
| Must be present in the Functional Profile|Yes, either verbatim or modified (e.g., constrained or refined)|Yes, verbatim.<br/>If dependency exists, add additional criteria reflecting the dependency.|
| Implemented by EHR systems|Yes.|Situational - only implement if the dependency exists.<br/>Specifically, the PHR system does not implement the ‘dependent shall’ criterion (as copied from the PHR-S FM), but does implement additional ‘shall’ criteria created to reflect the dependency.|
{: .grid .table-striped}

**Table 1: Differences between 'shall' and 'dependent shall'**

#### Rationale for ‘Dependent SHALL’

The reason for using a ‘dependent shall’ in the PHR-S FM is to highlight certain criteria and bring them to the
attention of the reader – both developers of functional profiles as well as other users. ‘Dependent shall’ criteria
are considered to be special cases, where there are one or more dependencies that affect these criteria,
across multiple care settings. Using the ‘dependent shall’ ensures that developers of all functional profiles
address the criterion and consciously decide whether the criterion in question is applicable, based on the
stated dependency.

Regardless of whether a dependency exists or not, the ‘dependent shall’ is copied verbatim into the functional
profile. The reasons for this are:

* Adherence to the rule that a ‘shall’ criterion is always inherited by the functional profile.
* Consistency with handling the ‘dependent shall’ under all conditions (i.e., when there are
dependencies and when there are not).
* Retention of the ‘dependent shall’ so that it is present for derived profiles.
* Retention of the ‘dependent shall’ so that it remains effective for this profile if future requirements
change (i.e., the dependency **MAY** not be applicable at this present time, but **MAY** be applicable in
the future due to changes in user role, organizational policy or jurisdictional law.

#### How to Apply the ‘Dependent SHALL’

The way to interpret and apply a ‘dependent shall’ criterion in a functional profile is as follows:

* Copy the criterion into the functional profile.
* Review the criterion and determine if any of the dependencies are applicable to the functional
profile.
* If a dependency exists:<br/>
If one or more dependencies are applicable to the functional profile (e.g., there are jurisdictional legal
requirements), add one or more ‘shall’ criteria that refine and further constrain the ‘dependent shall’ with
respect to the dependencies.

For the new criteria, add an explanation and/or citing for the dependency. For example, “Jurisdictional
legal requirements for this functional profile are defined by U.S. Federal Regulations HIPAA Security Rule
45 CFR Parts 160, 162 and 164”. The explanation or citing **MAY** be in an appendix. It is likely that multiple
criteria will reference the same explanation or citing.

Examples:

Functional Profile criteria

1. *The PHR-S **SHALL** provide the ability for PHR-S security administrators to grant authorizations to
principles in accordance with HIPAA*.*
2. *The PHR-S **SHALL** provide the ability for PHR-S security administrators to grant authorizations for roles
in accordance with 42 CFR Part 2*.*

*Dependency Explanation: *For a U.S. realm functional profile, the Health Insurance Portability and
Accountability Act of 1996 (HIPAA) as well as other jurisdictional legal requirements or other more
stringent requirements would be applied to ‘dependent shall’ criteria in the functional profile.*

<table class="grid">
<tr><th>PHR-S FM</th>
<th>Dependency Applicable?</th>
<th>Applicability</th>
<th>Functional Profile</th></tr>
<tr><td rowspan="4">Dependent SHALL</td><td rowspan="4">Yes</td><td>Mandatory</td><td>Copy SHALL from the PHR-S FM</td></tr>
<tr><td>Mandatory</td><td>Add additional criteria to reflect the dependencies. Use ‘shall’.</td></tr>
<tr><td>Mandatory</td><td>Add explanation or citing</td></tr>
<tr><td>Optional</td><td>Add additional criteria derived from ‘dependent shall’. Use ‘shall’, ‘should’ or ‘may’.</td></tr>
<caption>Table 4 Summary of actions when dependency exists</caption>
</table>

* If no dependency exists:<br/>
If no dependency is applicable to the functional profile (i.e., there are no user roles, organizational
policies, or jurisdictional legal requirements that apply), then document the rationale for deciding that
no dependencies apply. This explanation **MAY** be in an appendix. It is likely that this explanation will
apply to multiple ‘dependent shall’ criteria.

<table class="grid">
<tr><th>PHR-S FM</th>
<th>Dependency Applicable?</th>
<th>Applicability</th>
<th>Functional Profile</th></tr>
<tr><td rowspan="4">Dependent SHALL</td><td rowspan="4">No</td><td>Mandatory</td><td>Copy SHALL from the PHR-S FM</td></tr>
<tr><td>Mandatory</td><td>Add explanation</td></tr>
<tr><td>Optional</td><td>Add additional criteria derived from ‘dependent shall’. Use ‘shall’, ‘should’ or ‘may’.</td></tr>
<caption>Table 5 Summary of actions for when no dependencies</caption>
</table>

* Add additional criteria – regardless of whether a dependency exists or not.<br/>
It is always permissible for a functional profile to add new criteria. Add new criteria that are derived
from the ‘dependent shall’. Use any keyword: ‘shall’, ‘should’ or ‘may’ (see Section 5.4) in these new
criteria.

Examples:

1. *The PHR-S **SHOULD** provide the ability for PHR-S security administrators to grant authorizations
to principals.*
2. *The PHR-S **MAY** provide the ability for PHR-S security administrators to grant authorizations for
roles.*
3. *The PHR-S **SHOULD** provide the ability for PHR-S security administrators to grant authorizations
within contexts.*
4. *The PHR-S **SHALL** provide the ability for PHR-S security administrators to grant authorizations for
roles for organizations with ten employees or more.*
