# Patient

## Endpoint Usages

### GET Patient

GET /{id}

GET ?identifier=http://hl7.org/fhir/v2/0203|JHN:{hn}

GET ?identifier={id}

### PUT Patient

FhirPatch support for Patient demographic updates

### POST Patient

Create a new Patient
Used for website form imports, kiosk walk-ins, new patients using online booking
