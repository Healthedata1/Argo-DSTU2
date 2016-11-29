#### Complete Summary of the Mandatory Requirements

1.  Conditionally One clinical status in `Condition.clinicalStatus`
    -   [Invariants]
        -   required if `Condition.verificationStatus != ‘entered-in-error‘`
        -   not present if `Condition.verificationStatus = ‘entered-in-error‘`
    -   Condition.clinicalStatus is bound to [Condition Clinical Status Codes] value set
1.  One code in `Condition.verificationStatus`
    -   Condition.clnicalStatus is bound to [ConditionVerificationStatus] value set
1.  One Identification of the problem or health concern in `Condition.code`which has an [extensible](http://hl7.org/fhir/terminologies.html#extensible) binding to:
    -   [Problem Value Set] value set.
1.  One patient reference in `Condition.patient`



#### problems and health concerns category codes

The [Argonaut Condition Category Codes] supports the separate concepts of problems and health concerns in `Condition.category` in order for API consumers to be able to separate health concerns and problems. However this is not mandatory for 2015 certification.

  [extensible]: http://hl7.org/fhir/terminologies.html#extensible
  [Problem Value Set]: http://hl7.org/fhir/DSTU2/daf/valueset-daf-problem.html
  [Invariants]: http://hl7.org/fhir/conformance-rules.html#constraints
  [Condition Clinical Status Codes]: http://hl7.org/fhir/valueset-condition-clinical.html
  [ConditionVerificationStatus]: http://hl7.org/fhir/valueset-condition-ver-status.html
  [Argonaut Condition Profile]: http://hl7.org/fhir/us/daf/daf-condition.html
 [Argonaut Condition Category Codes]: valueset-condition-category.html
