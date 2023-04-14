# coKreat - Release v5.2.0 (Live)

### Major release

Release-5.2.0

### Minor releases

Release-5.1.1&#x20;

Release-5.1.2&#x20;

Release-5.1.3

### Document release version <a href="#document-release-version" id="document-release-version"></a>

| Project | Release Date  | Version |
| ------- | ------------- | ------- |
| cokreat | 05 April 2023 | v5.2.0  |

**Discussion thread:** [**Link**](https://github.com/Sunbird-coKreat/Community/discussions/49)

### **Objectives of the coKreat release 5.2.0:**

The Objective of coKreat **5.2.0** aims taken Other Building Block(inQuiry) Changes to coKreat

### **Objectives of the coKreat release 5.1.3:**

The Objective of coKreat **5.1.3.0** aims at fixing the known bugs for the release and designing to make the cokreat independent of Sunbird-ED. and In this Release we are Merged the Release 5.1.1.0 and Release 5.1.2.0&#x20;

### Scope:

coKreat product release features and issues are described in this version 5.1.3. This document contains a short description of bugs to the coKreat product.

### **Description of the Product Features**

**Release 5.1.1-Ekstep Contributor Scope:** [**Link**](https://project-sunbird.atlassian.net/issues/?filter=12693)

| Sl.no | JIRA Id | Issue Type        | Description                                                                        |
| ----- | ------- | ----------------- | ---------------------------------------------------------------------------------- |
| 1     | CO-105  | Minor Enhancement | Remove unused and redundant code from Reference web app                            |
| 2     | CO-123  | Minor Enhancement | Modify/Identify the test cases that are dependent on other BB                      |
| 3     | CO-126  | Bug               | Fix the circle ci dependencies failure after the packages update from Knowldg team |

**Release 5.1.2-Ekstep Contributor Scope:** [**Link**](https://project-sunbird.atlassian.net/issues/?filter=12716)

| Sl.no | JIRA Id                                                       | Issue Type        | Description                                                                                                                                                                |
| ----- | ------------------------------------------------------------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1     | [CO-158](https://project-sunbird.atlassian.net/browse/CO-158) | RFC               | Design: How to make CoKreat independent of Sunbird-ED dependencies for Framework, Content, User etc                                                                        |
| 2     | [CO-183](https://project-sunbird.atlassian.net/browse/CO-183) | RFC               | SCORM: Content support                                                                                                                                                     |
| 3     | [CO-79](https://project-sunbird.atlassian.net/browse/CO-79)   | Minor Enhancement | Migration of Reference Web App to Angular 12                                                                                                                               |
| 4     | [CO-108](https://project-sunbird.atlassian.net/browse/CO-108) | Bug               | Draft content count is getting displayed on unit node for the Contribution org reviewer and Contribution org contributor before the user with both role create the content |

**Release 5.1.3-Ekstep Contributor Scope:** [**Link**](https://project-sunbird.atlassian.net/issues/?filter=12736\&jql=project%20%3D%20CO%20AND%20issuetype%20in%20\(Bug%2C%20Documentation-Issue%2C%20Epic%2C%20Installation-Issues%2C%20Minor-Enhancement%2C%20RFC%2C%20Test\)%20AND%20%22Contributor%20Type%5BSelect%20List%20\(cascading\)%5D%22%20in%20cascadeOption\(10441%2C%2010443\)%20AND%20Sprint%20%3D%20333%20ORDER%20BY%20issuetype%20DESC%2C%20created%20DESC)

| Sl.no | JIRA Id                                                       | Issue Type          | Description                                                                                                  |
| ----- | ------------------------------------------------------------- | ------------------- | ------------------------------------------------------------------------------------------------------------ |
| 1     | [CO-274](https://project-sunbird.atlassian.net/browse/CO-274) | RFC                 | SCORM: Content support (continuation) - Part 2                                                               |
| 2     | [CO-268](https://project-sunbird.atlassian.net/browse/CO-268) | RFC                 | Design: How to make CoKreat independent of Sunbird-ED dependencies for Framework, Content, User etc - Part 2 |
| 3     | [CO-267](https://project-sunbird.atlassian.net/browse/CO-267) | Minor Enhancement   | Request traceability with proper logs (Part 2)                                                               |
| 4     | [CO-128](https://project-sunbird.atlassian.net/browse/CO-128) | Minor Enhancement   | Documentation on CoKreat installation package (separate and along with ED)                                   |
| 5     | [CO-289](https://project-sunbird.atlassian.net/browse/CO-289) | Documentation-Issue | Move all the relevant docs to microsite or postman                                                           |

**Release 5.2.0-Ekstep Contributor Scope:** [**Link**](https://project-sunbird.atlassian.net/issues/?jql=project%20%3D%20CO%20AND%20issuetype%20in%20standardIssueTypes\(\)%20AND%20Sprint%20%3D%20334%20ORDER%20BY%20key%20ASC%2C%20created%20DESC)

| Sl.no | JIRA Id                                                       | Issue Type        | Description                 |
| ----- | ------------------------------------------------------------- | ----------------- | --------------------------- |
| 1     | [CO-330](https://project-sunbird.atlassian.net/browse/CO-330) | Minor Enhancement | inQuiry: NPM package update |

**Samagra Contributor Scope:**&#x20;

| Sl.no | JIRA Id | Contributor | Issue Type        | Description |
| ----- | ------- | ----------- | ----------------- | ----------- |
| 1     |         | Ekstep      | Minor Enhancement |             |
| 2     |         | Ekstep      | Bug               |             |

### **Ekstep Contribution Test Scenarios:**&#x20;

**Release 5.1.1.0 Test Scenarios:** [**Link**](https://project-sunbird.atlassian.net/wiki/spaces/COK/pages/3272114311/R+5.1.1.0+Test+Scenarios)

**Release 5.1.2.0 Test Scenarios:** [**Link**](https://project-sunbird.atlassian.net/wiki/spaces/COK/pages/3272736991/R+5.1.2.0+Test+Scenarios)

**Release 5.1.3.0 Test Scenarios:** [**Link**](https://project-sunbird.atlassian.net/wiki/spaces/COK/pages/3272605728/R+5.1.3.0+Test+Scenarios)

**Release 5.2.0 Test Scenarios: NA**

### **Samagra Contribution Test Case:**&#x20;

### **Upgrade to release-5.1.3.0**:

#### Configurations:

| Variable Name                      | Service Name | Default Public Value | Private Value Override | Comments |
| ---------------------------------- | ------------ | -------------------- | ---------------------- | -------- |
| sunbird\_cloud\_storage\_key       | Player       |                      |                        |          |
| sunbird\_cloud\_storage\_secret    | Player       |                      |                        |          |
| sunbird\_cloud\_report\_container  | Player       | reports              |                        |          |
| sunbird\_cloud\_storage\_region    | Player       |                      |                        |          |
| sunbird\_cloud\_storage\_container | Player       |                      |                        |          |
| sunbird\_gcloud\_project\_id       | Player       |                      |                        |          |



**Sample configuration for ED:**

```
```

#### Jenkins Jobs:

| Service to be Build      | Build Tag | Service to Deploy         | Deploy Tag | Comments |
| ------------------------ | --------- | ------------------------- | ---------- | -------- |
| Build/Kubernetes/Player  |           | Deploy/Kubernetes/Player  |            |          |
| Build/Kubernetes/Program |           | Deploy/Kubernetes/Program |            |          |

Along with above service, we need to take latest changes from Knowlg and inQuiry building blocks  please use below release notes to deploy in coKreat.

### Dependency release tags

#### Sunbird Knowlg



#### Sunbird Inquiry



