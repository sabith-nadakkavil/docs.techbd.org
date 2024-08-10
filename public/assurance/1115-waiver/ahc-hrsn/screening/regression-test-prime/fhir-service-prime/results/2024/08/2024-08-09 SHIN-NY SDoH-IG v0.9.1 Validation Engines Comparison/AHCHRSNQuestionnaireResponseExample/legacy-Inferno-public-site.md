# File evaluation against Legacy Inferno public site

## Files tested

- [AHCHRSNQuestionnaireResponseExample.json](AHCHRSNQuestionnaireResponseExample.json)

## NYeC expectations

```json
{
  "testcase": AHCHRSNQuestionnaireResponseExample,
  "csvoutputS3Bucket": "certification-engine-output",
  "testcasetype": "POSITIVE",
  "expectedResult": "AHCHRSNQuestionnaireResponseExample should succcessfully be processed by the QE and forwarded to NYeC.  The MPI for the patient should be added to the Patient resource."
}
```

## Legacy Inferno public site

[https://inferno.healthit.gov/validator/](https://inferno.healthit.gov/validator/)

```
Validated the uploaded resource against the http://shinny.org/StructureDefinition/SHINNYBundleProfile StructureDefinition
Validation errors:
Bundle: Constraint failed: SHINNY-Bundle-Encounter-Location-RI: 'Checks for RI between Encounter & Location' (defined in http://shinny.org/StructureDefinition/SHINNYBundleProfile) on line 1. 
Bundle: Constraint failed: SHINNY-Bundle-Patient-Org-RI: 'Checks for RI between Patient & Assigning Org' (defined in http://shinny.org/StructureDefinition/SHINNYBundleProfile) on line 1. 
Bundle.meta: Unknown profile http://shinny.org/StructureDefinition/SHINNYMeta on line 4. 
Validation warnings:
Bundle.entry[1].resource/*Encounter/EncounterExample*/.subject: Entry 0 matches the reference Patient/PatientExample by type and id but it's fullUrl http://shinny.org/PatientExample does not match the full target URL http://Patient/PatientExample by Bundle resolution rules on line -1. 
Bundle.entry[2].resource/*Consent/ConsentExample*/.patient: Entry 0 matches the reference Patient/PatientExample by type and id but it's fullUrl http://shinny.org/PatientExample does not match the full target URL http://Patient/PatientExample by Bundle resolution rules on line -1. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.subject: Entry 0 matches the reference Patient/PatientExample by type and id but it's fullUrl http://shinny.org/PatientExample does not match the full target URL http://Patient/PatientExample by Bundle resolution rules on line -1. 
Bundle.entry[6].resource/*Observation/ObservationResponseHousingInstability71802-3*/.subject: Entry 0 matches the reference Patient/PatientExample by type and id but it's fullUrl http://shinny.org/PatientExample does not match the full target URL http://Patient/PatientExample by Bundle resolution rules on line -1. 
Bundle.entry[7].resource/*Observation/ObservationResponseInadequateHousing96778-6*/.subject: Entry 0 matches the reference Patient/PatientExample by type and id but it's fullUrl http://shinny.org/PatientExample does not match the full target URL http://Patient/PatientExample by Bundle resolution rules on line -1. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.subject: Entry 0 matches the reference Patient/PatientExample by type and id but it's fullUrl http://shinny.org/PatientExample does not match the full target URL http://Patient/PatientExample by Bundle resolution rules on line -1. 
Bundle.entry[9].resource/*Observation/ObservationResponseFinancialInsecurity76513-1*/.subject: Entry 0 matches the reference Patient/PatientExample by type and id but it's fullUrl http://shinny.org/PatientExample does not match the full target URL http://Patient/PatientExample by Bundle resolution rules on line -1. 
Bundle.entry[10].resource/*Observation/ObservationResponseEmploymentStatus96780-2*/.subject: Entry 0 matches the reference Patient/PatientExample by type and id but it's fullUrl http://shinny.org/PatientExample does not match the full target URL http://Patient/PatientExample by Bundle resolution rules on line -1. 
Bundle.entry[11].resource/*QuestionnaireResponse/QuestionnaireResponse-123*/.subject: Entry 0 matches the reference Patient/PatientExample by type and id but it's fullUrl http://shinny.org/PatientExample does not match the full target URL http://Patient/PatientExample by Bundle resolution rules on line -1. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.encounter: Entry 1 matches the reference Encounter/EncounterExample by type and id but it's fullUrl http://shinny.org/EncounterExample does not match the full target URL http://Encounter/EncounterExample by Bundle resolution rules on line -1. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.encounter: Entry 1 matches the reference Encounter/EncounterExample by type and id but it's fullUrl http://shinny.org/EncounterExample does not match the full target URL http://Encounter/EncounterExample by Bundle resolution rules on line -1. 
Bundle.entry[11].resource/*QuestionnaireResponse/QuestionnaireResponse-123*/.encounter: Entry 1 matches the reference Encounter/EncounterExample by type and id but it's fullUrl http://shinny.org/EncounterExample does not match the full target URL http://Encounter/EncounterExample by Bundle resolution rules on line -1. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.hasMember[1]: Entry 10 matches the reference Observation/ObservationResponseEmploymentStatus96780-2 by type and id but it's fullUrl http://shinny.org/ObservationResponseEmploymentStatus96780-2 does not match the full target URL http://Observation/ObservationResponseEmploymentStatus96780-2 by Bundle resolution rules on line -1. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.derivedFrom[0]: Entry 11 matches the reference QuestionnaireResponse/QuestionnaireResponse-123 by type and id but it's fullUrl http://shinny.org/QuestionnaireResponse-123 does not match the full target URL http://QuestionnaireResponse/QuestionnaireResponse-123 by Bundle resolution rules on line -1. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.derivedFrom[0]: Entry 11 matches the reference QuestionnaireResponse/QuestionnaireResponse-123 by type and id but it's fullUrl http://shinny.org/QuestionnaireResponse-123 does not match the full target URL http://QuestionnaireResponse/QuestionnaireResponse-123 by Bundle resolution rules on line -1. 
Bundle.entry[0].resource/*Patient/PatientExample*/.identifier[1].assigner: Entry 4 matches the reference Organization/InsuranceExample by type and id but it's fullUrl http://shinny.org/InsuranceExample does not match the full target URL http://Organization/InsuranceExample by Bundle resolution rules on line -1. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.hasMember[0]: Entry 6 matches the reference Observation/ObservationResponseHousingInstability71802-3 by type and id but it's fullUrl http://shinny.org/ObservationResponseHousingInstability71802-3 does not match the full target URL http://Observation/ObservationResponseHousingInstability71802-3 by Bundle resolution rules on line -1. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.hasMember[1]: Entry 7 matches the reference Observation/ObservationResponseInadequateHousing96778-6 by type and id but it's fullUrl http://shinny.org/ObservationResponseInadequateHousing96778-6 does not match the full target URL http://Observation/ObservationResponseInadequateHousing96778-6 by Bundle resolution rules on line -1. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.hasMember[0]: Entry 9 matches the reference Observation/ObservationResponseFinancialInsecurity76513-1 by type and id but it's fullUrl http://shinny.org/ObservationResponseFinancialInsecurity76513-1 does not match the full target URL http://Observation/ObservationResponseFinancialInsecurity76513-1 by Bundle resolution rules on line -1. 
Bundle.entry[0].resource/*Patient/PatientExample*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shinny-patient' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 12. 
Bundle.entry[0].resource/*Patient/PatientExample*/.identifier[1].type: None of the codings provided are in the value set 'IdentifierType' (http://hl7.org/fhir/ValueSet/identifier-type|4.0.1), and a coding should come from this value set unless it has no suitable code (note that the validator cannot judge what is suitable) (codes = http://terminology.hl7.org/CodeSystem/v2-0203#MA) on line 72. 
Bundle.entry[0].resource/*Patient/PatientExample*/.identifier[2].type: None of the codings provided are in the value set 'IdentifierType' (http://hl7.org/fhir/ValueSet/identifier-type|4.0.1), and a coding should come from this value set unless it has no suitable code (note that the validator cannot judge what is suitable) (codes = http://terminology.hl7.org/CodeSystem/v2-0203#SS) on line 85. 
Bundle.entry[1].resource/*Encounter/EncounterExample*/.meta.profile[1]: Profile reference 'http://shinny.org/StructureDefinition/shin-ny-encounter' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 137. 
Bundle.entry[1].resource/*Encounter/EncounterExample*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shinny-encounter' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 137. 
Bundle.entry[2].resource/*Consent/ConsentExample*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shinny-Consent' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 182. 
Bundle.entry[2].resource/*Consent/ConsentExample*/.meta.profile[1]: Profile reference 'http://shinny.org/StructureDefinition/shinny-consent' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 182. 
Bundle.entry[2].resource/*Consent/ConsentExample*/.scope: None of the codings provided are in the value set 'Consent Scope Codes' (http://hl7.org/fhir/ValueSet/consent-scope|4.0.1), and a coding should come from this value set unless it has no suitable code (note that the validator cannot judge what is suitable) (codes = null#treatment) on line 195. 
Bundle.entry[2].resource/*Consent/ConsentExample*/.scope.coding[0]: Coding has no system. A code with no system has no defined meaning, and it cannot be validated. A system should be provided on line 195. 
Bundle.entry[2].resource/*Consent/ConsentExample*/.category[0]: None of the codings provided are in the value set 'Consent Category Codes' (http://hl7.org/fhir/ValueSet/consent-category|4.0.1), and a coding should come from this value set unless it has no suitable code (note that the validator cannot judge what is suitable) (codes = null#59284-0) on line 201. 
Bundle.entry[2].resource/*Consent/ConsentExample*/.category[0].coding[0]: Coding has no system. A code with no system has no defined meaning, and it cannot be validated. A system should be provided on line 201. 
Bundle.entry[3].resource/*Organization/ProviderExample*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shin-ny-organization' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 224. 
Bundle.entry[3].resource/*Organization/ProviderExample*/.identifier[0].type: None of the codings provided are in the value set 'IdentifierType' (http://hl7.org/fhir/ValueSet/identifier-type|4.0.1), and a coding should come from this value set unless it has no suitable code (note that the validator cannot judge what is suitable) (codes = null#null) on line 236. 
Bundle.entry[3].resource/*Organization/ProviderExample*/.identifier[0].type.coding[0]: Coding has no system. A code with no system has no defined meaning, and it cannot be validated. A system should be provided on line 236. 
Bundle.entry[4].resource/*Organization/InsuranceExample*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shin-ny-organization' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 261. 
Bundle.entry[4].resource/*Organization/InsuranceExample*/.identifier[0].type: None of the codings provided are in the value set 'IdentifierType' (http://hl7.org/fhir/ValueSet/identifier-type|4.0.1), and a coding should come from this value set unless it has no suitable code (note that the validator cannot judge what is suitable) (codes = null#null) on line 273. 
Bundle.entry[4].resource/*Organization/InsuranceExample*/.identifier[0].type.coding[0]: Coding has no system. A code with no system has no defined meaning, and it cannot be validated. A system should be provided on line 273. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/: Best Practice Recommendation: In general, all observations should have a performer on line 302. 
Bundle.entry[5].resource: Best Practice Recommendation: In general, all observations should have a performer on line 302. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.meta.profile[1]: Profile reference 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 302. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 302. 
Bundle.entry[6].resource/*Observation/ObservationResponseHousingInstability71802-3*/: Best Practice Recommendation: In general, all observations should have a performer on line 384. 
Bundle.entry[6].resource: Best Practice Recommendation: In general, all observations should have a performer on line 384. 
Bundle.entry[6].resource/*Observation/ObservationResponseHousingInstability71802-3*/.meta.profile[1]: Profile reference 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 384. 
Bundle.entry[6].resource/*Observation/ObservationResponseHousingInstability71802-3*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 384. 
Bundle.entry[7].resource/*Observation/ObservationResponseInadequateHousing96778-6*/: Best Practice Recommendation: In general, all observations should have a performer on line 444. 
Bundle.entry[7].resource: Best Practice Recommendation: In general, all observations should have a performer on line 444. 
Bundle.entry[7].resource/*Observation/ObservationResponseInadequateHousing96778-6*/.meta.profile[1]: Profile reference 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 444. 
Bundle.entry[7].resource/*Observation/ObservationResponseInadequateHousing96778-6*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 444. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/: Best Practice Recommendation: In general, all observations should have a performer on line 512. 
Bundle.entry[8].resource: Best Practice Recommendation: In general, all observations should have a performer on line 512. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.meta.profile[1]: Profile reference 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 512. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 512. 
Bundle.entry[9].resource/*Observation/ObservationResponseFinancialInsecurity76513-1*/: Best Practice Recommendation: In general, all observations should have a performer on line 589. 
Bundle.entry[9].resource: Best Practice Recommendation: In general, all observations should have a performer on line 589. 
Bundle.entry[9].resource/*Observation/ObservationResponseFinancialInsecurity76513-1*/.meta.profile[1]: Profile reference 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 589. 
Bundle.entry[9].resource/*Observation/ObservationResponseFinancialInsecurity76513-1*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 589. 
Bundle.entry[10].resource/*Observation/ObservationResponseEmploymentStatus96780-2*/: Best Practice Recommendation: In general, all observations should have a performer on line 656. 
Bundle.entry[10].resource: Best Practice Recommendation: In general, all observations should have a performer on line 656. 
Bundle.entry[10].resource/*Observation/ObservationResponseEmploymentStatus96780-2*/.meta.profile[1]: Profile reference 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 656. 
Bundle.entry[10].resource/*Observation/ObservationResponseEmploymentStatus96780-2*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 656. 
Bundle.entry[11].resource/*QuestionnaireResponse/QuestionnaireResponse-123*/.meta.profile[0]: Profile reference 'http://shinny.org/StructureDefinition/shinny-questionnaire-response' has not been checked because it could not be found, and the validator is set to not fetch unknown profiles on line 723. 
Bundle.entry[11].resource/*QuestionnaireResponse/QuestionnaireResponse-123*/: The questionnaire 'http://shinny.org/fhir/Questionnaire/hrsn-questionnaire' could not be resolved, so no validation can be performed against the base questionnaire on line 734. 
Bundle.entry[11].resource: The questionnaire 'http://shinny.org/fhir/Questionnaire/hrsn-questionnaire' could not be resolved, so no validation can be performed against the base questionnaire on line 734. 
Validation information:
Bundle.entry[0].resource/*Patient/PatientExample*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shinny-patient' does not resolve on line 17. 
Bundle.entry[0].resource/*Patient/PatientExample*/.communication[0].language.coding[0].system: A definition for CodeSystem 'urn:iso:std:iso:639' could not be found, so the code cannot be validated on line 121. 
Bundle.entry[1].resource/*Encounter/EncounterExample*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shinny-encounter' does not resolve on line 142. 
Bundle.entry[1].resource/*Encounter/EncounterExample*/.meta.profile[1]: Canonical URL 'http://shinny.org/StructureDefinition/shin-ny-encounter' does not resolve on line 143. 
Bundle.entry[2].resource/*Consent/ConsentExample*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shinny-Consent' does not resolve on line 187. 
Bundle.entry[2].resource/*Consent/ConsentExample*/.meta.profile[1]: Canonical URL 'http://shinny.org/StructureDefinition/shinny-consent' does not resolve on line 188. 
Bundle.entry[3].resource/*Organization/ProviderExample*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shin-ny-organization' does not resolve on line 229. 
Bundle.entry[3].resource/*Organization/ProviderExample*/.type[0]: Reference to draft CodeSystem http://terminology.hl7.org/CodeSystem/organization-type|0.1.0 on line 245. 
Bundle.entry[4].resource/*Organization/InsuranceExample*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shin-ny-organization' does not resolve on line 266. 
Bundle.entry[4].resource/*Organization/InsuranceExample*/.type[0]: Reference to draft CodeSystem http://terminology.hl7.org/CodeSystem/organization-type|0.1.0 on line 283. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' does not resolve on line 307. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.meta.profile[1]: Canonical URL 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' does not resolve on line 308. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.category[0].coding[0]: A definition for CodeSystem 'http://hl7.org/fhir/us/sdoh-clinicalcare/CodeSystem/SDOHCC-CodeSystemTemporaryCodes' could not be found, so the code cannot be validated on line 315. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.category[0].coding[1]: A definition for CodeSystem 'http://hl7.org/fhir/us/sdoh-clinicalcare/CodeSystem/SDOHCC-CodeSystemTemporaryCodes' could not be found, so the code cannot be validated on line 315. 
Bundle.entry[5].resource/*Observation/AssessmentResponseQuestionGrouper1*/.category[0].coding[2]: A definition for CodeSystem 'http://hl7.org/fhir/us/sdoh-clinicalcare/CodeSystem/SDOHCC-CodeSystemTemporaryCodes' could not be found, so the code cannot be validated on line 315. 
Bundle.entry[6].resource/*Observation/ObservationResponseHousingInstability71802-3*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' does not resolve on line 389. 
Bundle.entry[6].resource/*Observation/ObservationResponseHousingInstability71802-3*/.meta.profile[1]: Canonical URL 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' does not resolve on line 390. 
Bundle.entry[6].resource/*Observation/ObservationResponseHousingInstability71802-3*/.category[0].coding[0]: A definition for CodeSystem 'http://hl7.org/fhir/us/sdoh-clinicalcare/CodeSystem/SDOHCC-CodeSystemTemporaryCodes' could not be found, so the code cannot be validated on line 397. 
Bundle.entry[7].resource/*Observation/ObservationResponseInadequateHousing96778-6*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' does not resolve on line 449. 
Bundle.entry[7].resource/*Observation/ObservationResponseInadequateHousing96778-6*/.meta.profile[1]: Canonical URL 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' does not resolve on line 450. 
Bundle.entry[7].resource/*Observation/ObservationResponseInadequateHousing96778-6*/.category[0].coding[0]: A definition for CodeSystem 'http://hl7.org/fhir/us/sdoh-clinicalcare/CodeSystem/SDOHCC-CodeSystemTemporaryCodes' could not be found, so the code cannot be validated on line 457. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' does not resolve on line 517. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.meta.profile[1]: Canonical URL 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' does not resolve on line 518. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.category[0].coding[0]: A definition for CodeSystem 'http://hl7.org/fhir/us/sdoh-clinicalcare/CodeSystem/SDOHCC-CodeSystemTemporaryCodes' could not be found, so the code cannot be validated on line 525. 
Bundle.entry[8].resource/*Observation/AssessmentResponseQuestionGrouper2*/.category[0].coding[1]: A definition for CodeSystem 'http://hl7.org/fhir/us/sdoh-clinicalcare/CodeSystem/SDOHCC-CodeSystemTemporaryCodes' could not be found, so the code cannot be validated on line 525. 
Bundle.entry[9].resource/*Observation/ObservationResponseFinancialInsecurity76513-1*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' does not resolve on line 594. 
Bundle.entry[9].resource/*Observation/ObservationResponseFinancialInsecurity76513-1*/.meta.profile[1]: Canonical URL 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' does not resolve on line 595. 
Bundle.entry[9].resource/*Observation/ObservationResponseFinancialInsecurity76513-1*/.category[0].coding[0]: A definition for CodeSystem 'http://hl7.org/fhir/us/sdoh-clinicalcare/CodeSystem/SDOHCC-CodeSystemTemporaryCodes' could not be found, so the code cannot be validated on line 602. 
Bundle.entry[10].resource/*Observation/ObservationResponseEmploymentStatus96780-2*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shin-ny-observation-screening-response' does not resolve on line 661. 
Bundle.entry[10].resource/*Observation/ObservationResponseEmploymentStatus96780-2*/.meta.profile[1]: Canonical URL 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ObservationScreeningResponse' does not resolve on line 662. 
Bundle.entry[10].resource/*Observation/ObservationResponseEmploymentStatus96780-2*/.category[0].coding[0]: A definition for CodeSystem 'http://hl7.org/fhir/us/sdoh-clinicalcare/CodeSystem/SDOHCC-CodeSystemTemporaryCodes' could not be found, so the code cannot be validated on line 669. 
Bundle.entry[11].resource/*QuestionnaireResponse/QuestionnaireResponse-123*/.meta.profile[0]: Canonical URL 'http://shinny.org/StructureDefinition/shinny-questionnaire-response' does not resolve on line 728. 
Bundle.entry[11].resource/*QuestionnaireResponse/QuestionnaireResponse-123*/.questionnaire: Canonical URL 'http://shinny.org/fhir/Questionnaire/hrsn-questionnaire' does not resolve on line 734. 
```