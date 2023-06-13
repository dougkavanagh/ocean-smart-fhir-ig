# Observation

Used to read and write observations relevant to Ocean's use cases. Observations are read by Ocean so that they can be included in form pre-population, particularly for eReferrals and eConsults, but also potentially for patient-facing forms. For example, Ocean may use the patient's most recent height, weight, blood pressure, creatinine, eGFR, hemoglobin, etc. as a value to be pre-populated in a referral form where this information is pertinent.

Ocean expects to read Observation instances via the $everything operation. It does not query for Observations separately.

However, Observation are used more extensively by Ocean to record new, structured, patient-reported values, such as clinical form score ("PHQ-9"), smoking status, patient experience scores, home blood pressure readings, and so on.

These values are often called PREMs (Patient Reported Experience Measures) and PROMs (Patient-Reported Outcome Measures).

Theoretically any Ocean form or product may produce an Observation worth recording in an EMR/EHR, whether it be an emailed form with Patient Messaging or Reminders``, a Website Form, a kiosk or tablet form, or even the pre-booking and post-booking forms used for OAB.

However, support for reading and writing of Observations is considered optional, since it is not typically required by the core use cases of the platform.

## Key Observation codes

To improve Ocean's clinical decision support, we strongly recommend that the following codes be used for certain key Observations. Some EMRs may store these particular observations within the patient's profile ("CPP") as opposed to a discrete date/value pair; in these cases, we recommend that you map these to an Observation using a best-effort estimate of the effective date (such as the modification date of the corresponding CPP field, or even the current date/time as a last resort).

- LOINC 72166-2 Tobacco smoking status - This reflects the official [Canadian Baseline](https://build.fhir.org/ig/HL7-Canada/ca-baseline/StructureDefinition-profile-smokingstatus.html) and should use the coded values [defined here](http://hl7.org/fhir/uv/ips/STU1/ValueSet-current-smoking-status-uv-ips.html)
- LOINC 63640-7 How many cigarettes per day do, or did, you smoke - use a valueString e.g. "5-10"
- LOINC 74013-4 Alcoholic drinks per day - use a valueString e.g. "5-10"
