# Practitioner

Practitioners are used by Ocean to determine the list of providers, generally for configuraton purposes. The list of practitioners are used in a number of ways during the configuration, typically as a picklist of "Providers" applied as a constraint to reminders or online booking rules. For example, users can set up an online booking schedule that is only accessible to patients with a certain Practitioner on their care team.
## Endpoint Usages

### GET Practitioner?active=true

As part of Ocean's periodic synchronization, it will fetch all the active Practitioner resources to determine the list of potential providers that may be configured.