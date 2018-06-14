# 1. Infrastructure overview
This is a Vicinity Adapter for Value Added Services of MPH Pilot Case.

# 2. Configuration and deployment
## Build using Maven

In the root folder of the project:

`mvn clean install`

## Deploy on Tomcat 8.5

Copy the SiteWhereAdapter-0.0.1-SNAPSHOT.war file from ./target directory of the project to /webapps directory located on Tomcat server and start Tomcat server
or 
use Manager web application http://host-IP:port/manager/html for deployment (you need manager-gui role to be allowed to access it).


# 3. Functionality and API

## Endpoints
* GET /objects (optional): Retrieve all devices Thing Descriptions(TDs) for registration to VICINITY. This functionality is optional since auto-registration will be performed, so the adapter will send the TDs to the agent at start-up.
* PUT /objects/{oid}/events/{eid}: This endpoint will be called each time the topic has changed in order to inform the VAS for new measurements
* POST / objects/{oid}/actions/{aid}
