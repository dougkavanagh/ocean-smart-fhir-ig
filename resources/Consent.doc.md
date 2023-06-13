# Consent

Consent is an optional resource that may be returned within the Patient/$everything Bundle. It may be used by Ocean to read and write the patient's consent status for email, SMS, Ocean use in general.

**SUBJECT TO CHANGE**

## Endpoint Usages

### POST /Consent

Ocean may post a Consent resource to the Consent endpoint to update the patient's consent status for email, SMS, and/or other forms of consent. The Consent resource will refer to the DocumentReference containing the consent form's generated note.

### GET /Patient/$everything

This resource may be returned in the $everything Bundle.
