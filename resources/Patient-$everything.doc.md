# Patient/$everything

This operation is used when uploading a patient to Ocean.

See the OperationDefinition in this guide for documentation on the Patient/$everything operation.

General information on the $everything operation from a FHIR perspective is provided here:
http://www.hl7.org/fhir/operation-patient-everything.html

Ocean uses the resulting Bundle to process any set of the following resources:
- AllergyIntolerance
- Appointment
- CareTeam
- Condition
- Consent
- DocumentReference
- Immunization
- MedicationStatement
- Observation
- Patient
- Practitioner
- Procedure
- QuestionnaireResponse

The Patient resource must be included in the Bundle.

Check the individual resource profiles for details on how these resources are used.

Generally Ocean will not expect to use resources older than 1-3 years old, so these may be omitted for performance reasons, unless they are non-expiring resources that are still clinically relevant. For example, an Observation for a blood pressure from 5 years ago may be omitted. However, an AllergyIntolerance to "pencillin" created 8 years ago is still very much clinically relevant and thus should be included in the result Bundle. Returning truly "everything" will satisfy these requirements but may lead to unacceptable performance. The trade-off here is left to the integrator to decide.