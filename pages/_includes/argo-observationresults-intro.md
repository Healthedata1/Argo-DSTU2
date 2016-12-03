Laboratory results are grouped and summarized using the [DiagnosticReport] resource which reference [Observation] resources.  Each Observation resource represents an individual laboratory test and result value, a “nested” panel (such as a microbial susceptibility panel) which references other observations, or rarely a laboratory test with component result values. This profile sets minimum expectations for the Observation resource resource to record, search and fetch laboratory test results associated with a patient.  It identifies which core elements, extensions, vocabularies and value sets **SHALL** be present in the resource when using this profile.

**Example Usage Scenarios:**

The following are example usage scenarios for the Argonaut Results profile:

-   Query for lab results belonging to a Patient
-   Record lab results belonging to a Patient

##### Mandatory Data Elements and Terminology


The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation.  Profile specific guidance and examples are provided as well.  The [**Formal Profile Definition**](#profile) below provides the  formal summary, definitions, and  terminology requirements.  

**Each Observation must have:**

1.   a status
1.   a category code of 'laboratory'
1.   a [LOINC] code, if available, which tells you what is being measured
1.   a patient
1.   a result value and, if the result value is a numeric quantity, a standard [UCUM] unit


Each Observation *should* have:

1.   a time indicating when the measurement was taken
1.   a reference range if available


**Profile specific implementation guidance:**

* Additional codes that translate or map to the Observation code or category codes are allowed.  For example:
   -  providing both a local system codes and a LOINC code that it map to
   -  providing a more specific category codes such as "chemistry', [SNOMED CT] concepts, or system specific codes in addition to the "laboratory" category code.
* If there is no result then you have to supply a reason unless Observation is being used to group other results then there is no value. Instead, it includes composite values or references to other Observations
* See the [General Guidance Section] for further guidance on using UCUM

#### Examples

- [Observation-usg](Observation-usg.html)
- [Observation-urobilinogen](Observation-urobilinogen.html)
- [Observation-urine-wbcs](Observation-urine-wbcs.html)
- [Observation-urine-sediment](Observation-urine-sediment.html)
- [Observation-urine-rbcs](Observation-urine-rbcs.html)
- [Observation-urine-protein](Observation-urine-protein.html)
- [Observation-urine-ph](Observation-urine-ph.html)
- [Observation-urine-nitrite](Observation-urine-nitrite.html)
- [Observation-urine-leukocyte-esterase](Observation-urine-leukocyte-esterase.html)
- [Observation-urine-ketone](Observation-urine-ketone.html)
- [Observation-urine-hemoglobin](Observation-urine-hemoglobin.html)
- [Observation-urine-glucose](Observation-urine-glucose.html)
- [Observation-urine-epi-cells](Observation-urine-epi-cells.html)
- [Observation-urine-color](Observation-urine-color.html)
- [Observation-urine-clarity](Observation-urine-clarity.html)
- [Observation-urine-cells](Observation-urine-cells.html)
- [Observation-urine-bilirubin](Observation-urine-bilirubin.html)
- [Observation-urine-bacteria](Observation-urine-bacteria.html)
- [Observation-serum-total-bilirubin](Observation-serum-total-bilirubin.html)
- [Observation-serum-sodium](Observation-serum-sodium.html)
- [Observation-serum-potassium](Observation-serum-potassium.html)
- [Observation-serum-creatinine](Observation-serum-creatinine.html)
- [Observation-serum-co2](Observation-serum-co2.html)
- [Observation-serum-chloride](Observation-serum-chloride.html)
- [Observation-serum-calcium](Observation-serum-calcium.html)
- [Observation-neutrophils](Observation-neutrophils.html)
- [Observation-mchc](Observation-mchc.html)
- [Observation-hemoglobin](Observation-hemoglobin.html)
- [Observation-erythrocytes](Observation-erythrocytes.html)
- [Observation-BUN](Observation-BUN.html)
- [Observation-blood-glucose](Observation-blood-glucose.html)

 [SNOMED CT]: http://snomed.info/sct
  [Observation Value Absent Reason]: http://hl7.org/fhir/valueset-observation-valueabsentreason.html
  [UCUM]: http://unitsofmeasure.org
  [LOINC]: http://loinc.org
[Observation]:  http://hl7.org/fhir/observation.html
[DiagnosticReport]:  http://hl7.org/fhir/diagnosticreport.html
[General Guidance Section]: definitions.html
