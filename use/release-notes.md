# Release Notes

| Release Date     | Version |
| ---------------- | ------- |
| 20 December 2023 | v7.0.0  |

### **Overview**



Discussion Thread:&#x20;

### Enhancements / Technical Tasks

1. &#x20;User deletion ([CO-668](https://project-sunbird.atlassian.net/browse/CO-668))

<details>

<summary>Details</summary>

From this release, coKreat Handled to delete the public users in Ed, who belong the following user roles in coKreat :

1. Individual contributor
2. Contributing org user

</details>

2. Generalisation of cKreate by removing hard Coded Values (i.e BMGS hardcode removal)([CO-586](https://project-sunbird.atlassian.net/browse/CO-586))

<details>

<summary>Details</summary>

Till 6.0.0, The framework categories i.e Board Medium Grade and Subject were hard coded in our system.

In this 7.0.0, the framework categories are not limited to Board Medium Grade and Subject, User can configure any category based on there framework requirements (eg. user can have different categories for agriculture framework and can have different categories for hospital framework), Also the number of categories will not be limited to four now user can have more than multiple categories.

We have removed all the hard codeings of the categories and made it genarilised using sb-forms and we will use the Client Service Library (sunbird NPM Package) to fetch thesse categories dynamically along with the form API which will have all the other validatuions, This API will work similar to exixting form API we use to create for SB forms.

We need to configure this form API with framework categories before we do the stating deployment to display all the categories&#x20;

You can refer to the postman collection [here](https://github.com/Sunbird-coKreat/docs/tree/main/postman/coKreat)

</details>

3. Node version Upgrades([CO-606](https://project-sunbird.atlassian.net/browse/CO-606) and [CO-607](https://project-sunbird.atlassian.net/browse/CO-607))

<details>

<summary>Details</summary>

In this upgraded program service node version to 14 and upgraded portal node version to 16

</details>

4. Question set editor integration([CO-384](https://project-sunbird.atlassian.net/browse/CO-384))

<details>

<summary>Details</summary>

As part of this we have to integration the question-set editor after upgrading to 14

</details>





### Open / Known Issues

* In Details and Filter page all the categories will come&#x20;
* We need to configure the editor forms and the primary category forms&#x20;

### coKreat Build Tags

| Service to be Build                         | Build Tag          | Service to Deploy                                                                                                                                                                                                                                                                                                  | Deploy Tag | Comments |
| ------------------------------------------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | -------- |
| <p></p><p>Build/Kubernetes/Player</p>       | release-7.0.0\_RC1 | Deploy/Kubernetes/Player                                                                                                                                                                                                                                                                                           |            |          |
| Build/Kubernetes/Program                    | release-7.0.0\_RC1 | Deploy/Kubernetes/Program                                                                                                                                                                                                                                                                                          |            |          |
| Build/DockKnowledgePlatform/CoKreatFlinkJob | release-7.0.0\_RC1 | <p><a href="http://10.20.0.14:8080/jenkins/job/Deploy/job/DockDev/job/KnowledgePlatform/job/CoKreatFlinkJob/">http://10.20.0.14:8080/jenkins/job/Deploy/job/DockDev/job/KnowledgePlatform/job/CoKreatFlinkJob/</a><br><br><br>This above service is in DEV env, Please create this is Staging environment also</p> |            |          |

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



### Inquiry Form Configurations: [Link](https://inquiry.sunbird.org/use/release-notes/inquiry-release-v6.0.0#form-field-config-change-as-per-quml-spec-1.1)

### **Ekstep Contributor Scope:**[ **Link**](https://project-sunbird.atlassian.net/issues/?filter=12846\&jql=project%20%3D%20CO%20AND%20issuetype%20in%20\(Documentation-Issue%2C%20Epic%2C%20Minor-Enhancement%2C%20RFC\)%20AND%20status%20in%20\(%22In%20Progress%22%2C%20Closed%2C%20Done%2C%20%22In%20Development%22%2C%20%22In%20Validation%22%2C%20%22Selected%20for%20Contribution%22\)%20AND%20Sprint%20in%20\(490%2C%20491%2C%20449\)%20AND%20assignee%20in%20\(currentUser\(\)%2C%20640855d981de11a1adfc7b17\))

### **Test Cases:** [**Link**](https://docs.google.com/spreadsheets/d/1Wkq73Z3E7vZ8DK8J9o1GOAV4V0CmtdG97btzueEuVW8/edit#gid=863875922)

### **Test case execution sheet:** [**Link**](https://docs.google.com/spreadsheets/d/1Wkq73Z3E7vZ8DK8J9o1GOAV4V0CmtdG97btzueEuVW8/edit#gid=863875922)



