# Release Notes

| Release Date | Version |
| ------------ | ------- |
| 26 Jun 2024  | v6.0.2  |
| 29 Sep 2023  | v6.0.1  |
| 29 June 2023 | v6.0.0  |

### **Overview**

v6.0.0 -> Angular upgrade of coKreat portal from 11-14 is done in this release.

v6.0.1 -> This release majorly highlights the CSP changes and angular upgrades. coKreat is now cloud agnostic; it will run seamlessly on any cloud service.

v6.0.2 -> This release has rigorously tested on Oracle Cloud Infrastructure (OCI). There was some fixes related to admin/org related reports  & OCI integration changes.

**6.0.2 issues fixed:**

* OCI integration CSP changes ([CO-874](https://project-sunbird.atlassian.net/browse/CO-874))

Discussion Thread: [https://github.com/orgs/Sunbird-coKreat/discussions/87](https://github.com/orgs/Sunbird-coKreat/discussions/87)

### Enhancements / Technical Tasks

1. coKreat is now cloud-agnostic ([co-514](https://project-sunbird.atlassian.net/browse/CO-514))

<details>

<summary>Details</summary>

From this release, coKreat proudly supports cloud agnosticity, allowing you to deploy and run the platform seamlessly across various cloud providers. This means you have the freedom to choose the cloud environment that best suits your organization's needs, whether it's AWS, Azure, Google Cloud, or others.

\
For more details on the node services, backend services, and file upload plugins, refer [CSP changes](https://ed.sunbird.org/\~/changes/c4YpJpIRZcszTUHGkkDJ/use/developer-guide/csp-changes)

</details>

2. Angular Upgrades

<details>

<summary>Details</summary>

Angular migration is completed for coKreat from v11 to v14

</details>

3. Removing unused and redundant code&#x20;

<details>

<summary>Details</summary>

Some time of the release was planned to remove unused and redundant code from coKreat and make the code more reusable and readable

</details>

4. Reduce spacing in the table in print preview ([co-316](https://project-sunbird.atlassian.net/browse/CO-316)) : _**Prashnavali**_
5. The basic details at the top of the paper and the Options lables for MCQ questions (क), ख), ग), घ) should be in Hindi, when medium of instruction is chosen as Hindi ([co-229](https://project-sunbird.atlassian.net/browse/CO-229)) : _**Prashnavali**_
6. Increasing test coverage percentage

<details>

<summary>Details</summary>

Test coverage percentage is now 38%

</details>

4. Postman collection for Object Categories and category definitions&#x20;
5. Architecture and component diagrams for coKreat and updating same in the micro-site
6. Architecture diagram, Data models and APIs for Contribution Service and updating same in the micro-site

### Bug Fixes

1. Program-service: Cert issue to access dev sunbird endpoint ([co-441](https://project-sunbird.atlassian.net/browse/CO-441))
2. The program publish api is failing when copying the collection from Ed portal to cokreat ([co-452](https://project-sunbird.atlassian.net/browse/CO-452))

### coKreat Build Tags

| Service to be Build      | Build Tag     | Service to Deploy         | Deploy Tag         | Comments |
| ------------------------ | ------------- | ------------------------- | ------------------ | -------- |
| Build/Kubernetes/Player  | release-6.0.1 | Deploy/Kubernetes/Player  | release-6.0.1\_RC3 |          |
| Build/Kubernetes/Program | release-6.0.1 | Deploy/Kubernetes/Program | release-6.0.1\_RC1 |          |

### Build Tags for other dependant BBs

The build tags used by the below building blocks for this release to upgrade coKreat are:&#x20;

[Sunbird ED](https://ed.sunbird.org/use/release/updating-sunbird-releases/5.2.0-to-6.0.0#sunbirded)

[Sunbird Lern](https://ed.sunbird.org/use/release/updating-sunbird-releases/5.2.0-to-6.0.0#sunbird-lern)

[Sunbird Obsrv](https://ed.sunbird.org/use/release/updating-sunbird-releases/5.2.0-to-6.0.0#sunbird-obsrv)

[Sunbird Knowlg](https://ed.sunbird.org/use/release/updating-sunbird-releases/5.2.0-to-6.0.0#sunbird-knowlg)

[Sunbird Inquiry](https://ed.sunbird.org/use/release/updating-sunbird-releases/5.2.0-to-6.0.0#sunbird-inquiry)

### Release Notes: Dependent building blocks

Sunbird-Knowlg: [v 5.5.0](https://knowlg.sunbird.org/use/release-notes/release-5.5.0-latest)

Sunbird-Obsrv: [v 5.1.0](https://obsrv.sunbird.org/use/release-notes/release-v-5.1.0)

Sunbird-Lern: [v 5.3.0](https://lern.sunbird.org/use/release-notes/release-v-5.3.0)

_**Note**: Only PII changes are taken in this release. RC migration is planned for future releases._

Sunbird-inQuiry: [v 5.7.0](https://inquiry.sunbird.org/use/release-notes/inquiry-release-v5.7.0-latest)

_**Note**_: _Question set editor is not integrated, planned for future releases._

Sunbird-CoKreat: [v 5.2.0](https://cokreat.sunbird.org/use/release-notes/cokreat-release-v5.2.0-upcoming-release)



### Configuration / Environment Variables Changes

This section provides a list of environment variables with their default values and descriptions required to run either the coKreat portal To change the default behaviour, modify the variable value based on your requirements.

<table><thead><tr><th width="161">Variable Name</th><th width="144">Service Name</th><th width="196">Default Public Value</th><th width="126">Private Value Override</th><th width="189">Comments</th></tr></thead><tbody><tr><td>sunbird_cloud_storage_key</td><td>Player</td><td></td><td></td><td></td></tr><tr><td>sunbird_cloud_storage_secret</td><td>Player</td><td></td><td></td><td></td></tr><tr><td>sunbird_cloud_report_container</td><td>Player</td><td>reports</td><td></td><td></td></tr><tr><td>sunbird_cloud_storage_region</td><td>Player</td><td></td><td></td><td></td></tr><tr><td>sunbird_cloud_storage_container</td><td>Player</td><td></td><td></td><td></td></tr><tr><td>sunbird_gcloud_project_id</td><td>Player</td><td></td><td></td><td></td></tr></tbody></table>



### **Ekstep Contributor Scope:**[ **Link**](https://project-sunbird.atlassian.net/issues/?filter=12810)

### **Test Cases:** [**Link**](https://docs.google.com/spreadsheets/d/1v3YnczXlEYd8UhHUHofY6meHqYni6cZjboE5eVU40N0/edit#gid=1378760827)

### **Test case execution sheet:** [**Link**](https://docs.google.com/spreadsheets/d/1v3YnczXlEYd8UhHUHofY6meHqYni6cZjboE5eVU40N0/edit#gid=1378760827)

### Migration scripts:

Please refer below documents for CSP migration for coKreat

{% embed url="https://project-sunbird.atlassian.net/wiki/spaces/SingleSource/pages/3258843156/coKreat+-+Data+Cloud+Agnostic+migration+scripts" %}

