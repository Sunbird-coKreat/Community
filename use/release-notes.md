# Release Notes

| Release Date     | Version |
| ---------------- | ------- |
| 20 December 2023 | v7.0.0  |

### **Overview**



Discussion Thread:&#x20;

### Enhancements / Technical Tasks

1. &#x20;User deletion ([co-](https://project-sunbird.atlassian.net/browse/CO-514)668)

<details>

<summary>Details</summary>

From this release, coKreat proudly supports cloud agnosticity, allowing you to deploy and run the platform seamlessly across various cloud providers. This means you have the freedom to choose the cloud environment that best suits your organization's needs, whether it's AWS, Azure, Google Cloud, or others.

\
For more details on the node services, backend services, and file upload plugins, refer [CSP changes](https://ed.sunbird.org/\~/changes/c4YpJpIRZcszTUHGkkDJ/use/developer-guide/csp-changes)

</details>

2. BMGS hardcode removal

<details>

<summary>Details</summary>

Till v6.0.0 BMGS i.e&#x20;

</details>

3. Node version Upgrades

<details>

<summary>Details</summary>

Some time of the release was planned to remove unused and redundant code from coKreat and make the code more reusable and readable

</details>

4. Question set editor integration

### Bug Fixes

1. Program-service: Cert issue to access dev sunbird endpoint ([co-441](https://project-sunbird.atlassian.net/browse/CO-441))
2. The program publish api is failing when copying the collection from Ed portal to cokreat ([co-452](https://project-sunbird.atlassian.net/browse/CO-452))

### coKreat Build Tags

| Service to be Build      | Build Tag     | Service to Deploy         | Deploy Tag | Comments |
| ------------------------ | ------------- | ------------------------- | ---------- | -------- |
| Build/Kubernetes/Player  | release-7.0.0 | Deploy/Kubernetes/Player  |            |          |
| Build/Kubernetes/Program | release-7.0.0 | Deploy/Kubernetes/Program |            |          |

### Build Tags for other dependant BBs

The build tags used by the below building blocks for this release to upgrade coKreat are:&#x20;

[Sunbird ED](https://ed.sunbird.org/use/release/updating-sunbird-releases/5.2.0-to-6.0.0#sunbirded)

[Sunbird Lern](https://ed.sunbird.org/use/release/updating-sunbird-releases/5.2.0-to-6.0.0#sunbird-lern)

[Sunbird Obsrv](https://ed.sunbird.org/use/release/updating-sunbird-releases/5.2.0-to-6.0.0#sunbird-obsrv)

[Sunbird Knowlg](https://ed.sunbird.org/use/release/updating-sunbird-releases/5.2.0-to-6.0.0#sunbird-knowlg)

[Sunbird Inquiry](https://ed.sunbird.org/use/release/updating-sunbird-releases/5.2.0-to-6.0.0#sunbird-inquiry)

### Release Notes: Dependent building blocks

Sunbird-Knowlg: [v ](https://knowlg.sunbird.org/use/release-notes/release-5.5.0-latest)7.0.0

Sunbird-Obsrv: [v 5.1.0](https://obsrv.sunbird.org/use/release-notes/release-v-5.1.0)

Sunbird-Lern: [v ](https://lern.sunbird.org/use/release-notes/release-v-5.3.0)7.0.0

_**Note**: Only PII changes are taken in this release. RC migration is planned for future releases._

Sunbird-inQuiry: [v ](https://inquiry.sunbird.org/use/release-notes/inquiry-release-v5.7.0-latest)7.0.0

### Configuration / Environment Variables Changes

This section provides a list of environment variables with their default values and descriptions required to run either the coKreat portal To change the default behaviour, modify the variable value based on your requirements.

<table><thead><tr><th width="161">Variable Name</th><th width="144">Service Name</th><th width="196">Default Public Value</th><th width="126">Private Value Override</th><th width="189">Comments</th></tr></thead><tbody><tr><td><p></p><p>program_service_baseurl</p></td><td>Flink Job</td><td></td><td><a href="http://{{private_ingressgateway_ip}}/program">http://{{private_ingressgateway_ip}}/program</a></td><td>The Program Serice base url param needed by coKreat-user-delete flink job to trigger DELETE user/{userId} API</td></tr><tr><td>sunbird_instance</td><td>Flink Job</td><td></td><td>sunbirddev</td><td>Sunbird instance</td></tr><tr><td>sunbird_kafka_brokers</td><td>Flink Job</td><td></td><td>{{groups['processing-cluster-kafka']|join(':9092,')}}:9092</td><td>coKreat-user-delete flink job will listen to the kafka event on set server.</td></tr><tr><td>sunbird_zookeepers</td><td>Flink Job</td><td></td><td>{{groups['processing-cluster-zookeepers']|join(':2181,')}}:2181</td><td></td></tr><tr><td>cokreat_user_delete_kafka_topic</td><td>Program</td><td></td><td>{{env}}.delete.user</td><td>DELETE program/v1/user/{userId} API, will generate the kafka event in set kafka topic</td></tr></tbody></table>



### **Ekstep Contributor Scope:**[ **Link**](https://project-sunbird.atlassian.net/issues/?filter=12810)

### **Test Cases:** [**Link**](https://docs.google.com/spreadsheets/d/1v3YnczXlEYd8UhHUHofY6meHqYni6cZjboE5eVU40N0/edit#gid=1378760827)

### **Test case execution sheet:** [**Link**](https://docs.google.com/spreadsheets/d/1v3YnczXlEYd8UhHUHofY6meHqYni6cZjboE5eVU40N0/edit#gid=1378760827)



