---
description: D
---

# cokreat- Release v5.1.0 (Upcoming release)

### Document release version <a href="#document-release-version" id="document-release-version"></a>

| Project | Release Date | Version |
| ------- | ------------ | ------- |
| cokreat | 28 Nov 2022  | v5.1.0  |

### **Objectives of the coKreat release v5.1.0**

The Objective of coCkreat **5.1.0** aims at fixing the known bugs for the release and make the cokreat portal as cloud agnostic.

### Scope:

coKreat product release features and issues are described in this version 5.1.0. This document contains a short description of bugs to the coKreat product.

### **Summary of the Product Features:**

This document contains information on the following existing bugs of the coKreat product

### **Description of the Product Features**

**Ekstep Contributor Scope:** [**Link**](https://project-sunbird.atlassian.net/issues/?filter=12683)****

**Samagra Contributor Scope:** [**Link**](https://project-sunbird.atlassian.net/issues/?filter=12692)****

| Sl.no | JIRA Id                                                       | Contributor | Issue Type        | Description                                                                    |
| ----- | ------------------------------------------------------------- | ----------- | ----------------- | ------------------------------------------------------------------------------ |
| 1     | [CO-140](https://project-sunbird.atlassian.net/browse/CO-140) | Ekstep      | Minor Enhancement | CSP Implementation: Cloud Agnostic report storage implementation               |
| 2     | [CO-113](https://project-sunbird.atlassian.net/browse/CO-113) | Ekstep      | Bug               | CLONE - User is able to delete draft content in the TOC post project end date. |
| 3     | [CO-90](https://project-sunbird.atlassian.net/browse/CO-90)   | Samagra     | Bug               |                                                                                |
| 4     | [CO-84](https://project-sunbird.atlassian.net/browse/CO-84)   | Samagra     | Bug               |                                                                                |
| 5     | [CO-95](https://project-sunbird.atlassian.net/browse/CO-95)   | Samagra     | Bug               |                                                                                |
| 6     | [CO-16](https://project-sunbird.atlassian.net/browse/CO-16)   | Samagra     | RFC               |                                                                                |
| 7     | [CO-118](https://project-sunbird.atlassian.net/browse/CO-118) | Samagra     | Bug               |                                                                                |

### **Ekstep Contribution Test Scenarios:** [**Link**](https://project-sunbird.atlassian.net/wiki/spaces/COK/pages/3250749445/R+5.1.0+Test+Scenarios)****

### **Samagra Contribution Test Case:** [**Link**](https://docs.google.com/spreadsheets/d/1-2dVsYG0N9C5n\_UndA6DAzwTGVjr-QX1KE\_LC5a7Wkc/edit#gid=0)****

### **Upgrade to release-5.1.0**:

| Variable Name                      | Service Name | Default Public Value | Private Value Override | Comments |
| ---------------------------------- | ------------ | -------------------- | ---------------------- | -------- |
| sunbird\_cloud\_storage\_key       | Player       |                      |                        |          |
| sunbird\_cloud\_storage\_secret    | Player       |                      |                        |          |
| sunbird\_cloud\_report\_container  | Player       | reports              |                        |          |
| sunbird\_cloud\_storage\_region    | Player       |                      |                        |          |
| sunbird\_cloud\_storage\_container | Player       |                      |                        |          |
| sunbird\_gcloud\_project\_id       | Player       |                      |                        |          |

| Service to be Build     | Build Tag          | Service to Deploy        | Deploy Tag             | Comments |
| ----------------------- | ------------------ | ------------------------ | ---------------------- | -------- |
| Build/Kubernetes/Player | release-5.1.0\_RC3 | Deploy/Kubernetes/Player | release-5.1.0-vdn\_RC1 |          |

Along with above service, we need to take latest changes from Knowlg and inQuiry building blocks  please use below release notes to deploy in coKreat.

{% embed url="https://knowlg.sunbird.org/use/release-notes/release-5.2.0-ongoing" %}
knowlg release notes
{% endembed %}

{% embed url="https://inquiry.sunbird.org/use/release-notes/inquiry-release-v5.2.0-live" %}
inQuiry release notes
{% endembed %}

#### Migration scripts:

Please refer below documents for CSP migration for coKreat

{% embed url="https://project-sunbird.atlassian.net/wiki/spaces/SingleSource/pages/3258843156/coKreat+-+Data+Cloud+Agnostic+migration+scripts" %}

