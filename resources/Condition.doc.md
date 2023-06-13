# Condition

Condition is an optional resource used to read and write to the patient's problem list and medical history.

**SUBJECT TO CHANGE**

## Endpoint Usages

### POST /Condition

Ocean may post a Condition when updating the patient's problem list or past medical history. To do so, the completed form must include a field [tagged with one of these values](https://support.cognisantmd.com/hc/en-us/articles/204782718-Setting-an-Ocean-eForm-to-Update-an-EMR-Demographic-Field).

### GET /Patient/$everything

This resource may be returned in the $everything Bundle.
