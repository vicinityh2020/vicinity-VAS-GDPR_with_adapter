# 1. Infrastructure overview
Vicinity Adapter for GDPR Value Added Service of MPH Pilot Case.

# 2. Configuration and deployment
## Build using Maven

In the root folder of the project:

`mvn clean install`


# 3. Functionality and API

## Endpoints
* GET /objects (optional): Retrieve all devices Thing Descriptions(TDs) for registration to VICINITY. This functionality is optional since auto-registration will be performed, so the adapter will send the TDs to the agent at start-up.
* PUT /objects/{oid}/events/{eid}: This endpoint will be called each time the topic has changed in order to inform the VAS for new measurements
* POST / objects/{oid}/actions/{aid}
