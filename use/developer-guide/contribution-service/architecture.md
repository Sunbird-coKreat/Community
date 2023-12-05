# Architecture

## System Context architecture



<figure><img src="../../../.gitbook/assets/programService-l0 (1).png" alt=""><figcaption></figcaption></figure>

## Flow Diagram



<figure><img src="../../../.gitbook/assets/programService-l1 (1).png" alt=""><figcaption></figcaption></figure>

Contribution (Program) service, offers the APIs for creating and managing projects, their nominations, setting and reading user preferences, reading the configuration, getting the list of tenants and projects reports, etc. It stores information about the sourcing projects, their nominations, and configuration.

**Routes**\
&#x20;\
It handles all the API routes triggering from portal with end point program/\*

**Request Middleware**

Request middleware provide methods to validate the tokens passed through API headers, create and validate request body, create response object etc.

Then if required forwards the request to service file who performs the CRUD operations on underlying tables and send back response.

For some API calls, request middleware if required gets details from other BB services, and send Response back to coKreat Portal

**Telemetry**

Telemetry service from Sunbird Util services is used to generate telemetry logs.

**Services From Other BBs**

Contribution (Program) service is integrated with services from different BBs.&#x20;

APIs which handles User Org data, utilised User org services to fecth user and org details. Organisation details are read using Org read API from UserOrg whereas User details are read using user Read or serch API.

Notification service is used to send out the email and sms notifications to the users. \
\
Content service is used to get the content or collection details, collection hierarchy, search the contents and collections with specific request.

Open Saber service is used to get the user, org, user\_org  details from the registry.

**Datastore**

Postgres is primary datastore for Programs, nominations, forms. Redis is used for caching the user preferences.

**Kafka**

Kafka events are generated for the question bulk creation APIs

{% embed url="https://youtu.be/l5BPgKYHfTs?feature=shared&t=566" %}
