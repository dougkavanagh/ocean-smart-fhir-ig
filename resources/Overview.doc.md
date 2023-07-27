Here’s an example Bundle containing instances of each resource type:
https://simplifier.net/Ocean-SMART-on-FHIR-Profiles/resources-Bundle-eg/~json

The project has documentation and several examples for the relevant FHIR resources:
• MedicationStatement
• Condition (“current” items for problem list, “resolved” items for past medical history)
• FamilyMemberHistory
• AllergyIntolerance
• Immunization
• Observation (for lab values, vitals, and smoking/alcohol status)
• DocumentReference (for attachments)
The profiles emphasize the text content of CPP items, i.e., the resource’s Narrative, text.div. Whether it’s an Immunization or a Condition or a FamilyMemberHistory, Ocean is going to grab the text.div content and use it to pre-populate the referral form values.

This text-first strategy aligns with the WYSISWYG nature of the patient’s CPP. It’s what Ocean does with the legacy SSO/contextual launch flows for PSS/MA/Accuro/OSCAR as well. It also simplifies the implementation: the CHR team can focus on populating the human-readable text of these items rather than worrying about coding.

Exception: The coding for Observations matters; Observations should have valid LOINC codes when possible. The actual value can be either structured (via valueQuantity) or textual (via valueString). Ocean is going to populate the text value in the form either way. Generally you shouldn’t have to do any specific LOINC mapping for the observations since they ought to already be stored in the lab values within the EMR. However, there are a few cases to be mindful of:
8302-2 - for height
29463-7 - for weight
35094-2 - for bp
38483-4 - for cr
45066-8 - for eGFR
59261-8 - for Hb A1C
(Plus the smoking/alcohol/drug use values you can see in the bundle)
