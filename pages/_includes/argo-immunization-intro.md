his profile sets minimum expectations for the [Immunization] resource to record, fetch and search immunization history associated with a patient. It identifies which core elements, extensions, vocabularies and value sets **SHALL** be present in the resource when using this profile.

**Example Usage Scenarios:**

The following are example usage scenarios for the Argonaut Immunization
profile:

-   Query for immunizations belonging to a Patient
-   Query for all patients who have had a specific vaccine administered

##### Mandatory Data Elements and Terminology


The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation.  Profile specific guidance and examples are provided as well.  The [**Formal Profile Definition**](#profile) below provides the  formal summary, definitions, and  terminology requirements.  

**Each Immunization must have:**

1.  a status
1.  a date the vaccine was administered
1.  a vaccine code that identifies the kind of vaccine administered
1.  a patient
1.  a flag to indicate whether vaccine was given
1.  a flag to indicate whether the vaccine was reported by patient rather than directly administered.


**Profile specific implementation guidance:**

* **NDC codes as a translational data element**:
Based upon the 2015 Edition Certification Requirements, [CVX vaccine codes] are required and the [NDC vaccine codes] SHOULD be supported as translations to them.  A NDC to [CVX crosswalk table] is also provided by the CDC.

#### Examples

   - [AllergyIntolerance-23](AllergyIntolerance-23.html)

  [CVX vaccine codes]: http://www2a.cdc.gov/vaccines/iis/iisstandards/vaccines.asp?rpt=cvx
  [NDC vaccine codes]: http://www2a.cdc.gov/vaccines/iis/iisstandards/ndc_crosswalk.asp
  [CVX crosswalk table]: http://www2a.cdc.gov/vaccines/iis/iisstandards/ndc_crosswalk.asp
[Immunization]:  http://hl7.org/fhir/immunization.html
