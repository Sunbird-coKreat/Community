# cokreat- Release v6.0.0 (Upcoming release)

### Document release version <a href="#document-release-version" id="document-release-version"></a>

| Project | Release Date | Version |
| ------- | ------------ | ------- |
| cokreat | 01 June 2023 | v6.0.0  |

### **Objectives of the coKreat release v6.0.0**

The Objective of cokreat **6.0.0** aims Angular Changes from 11 to 12, Angular 12 to 13 and Angualr 13 to14

### Scope:

coKreat product release features and issues are described in this version 6.0.0. This document contains a short description of bugs to the coKreat product.

### **Summary of the Product Features:**

This document contains information on the following existing bugs of the coKreat product

### **Description of the Product Features**

**Ekstep Contributor Scope:**[ **Link**](https://project-sunbird.atlassian.net/issues/?filter=12789)

**Samagra Contributor Scope:** [**Link**](https://project-sunbird.atlassian.net/issues/?filter=12692)

| Sl.no | JIRA Id | Contributor | Issue Type        | Description |
| ----- | ------- | ----------- | ----------------- | ----------- |
| 1     |         | Ekstep      | Minor Enhancement |             |
| 3     |         | Samagra     | Bug               |             |
| 4     |         | Samagra     | Bug               |             |
| 5     |         | Samagra     | Bug               |             |
| 6     |         | Samagra     | RFC               |             |
| 7     |         | Samagra     | Bug               |             |

### **Ekstep Contribution Test Scenarios:** [**Link**](https://project-sunbird.atlassian.net/wiki/spaces/COK/pages/3250749445/R+5.1.0+Test+Scenarios)

### **Samagra Contribution Test Case:** [**Link**](https://docs.google.com/spreadsheets/d/1-2dVsYG0N9C5n\_UndA6DAzwTGVjr-QX1KE\_LC5a7Wkc/edit#gid=0)

### **Upgrade to release-5.1.0**:

#### Configurations:

| Variable Name                      | Service Name | Default Public Value | Private Value Override | Comments |
| ---------------------------------- | ------------ | -------------------- | ---------------------- | -------- |
| sunbird\_cloud\_storage\_key       | Player       |                      |                        |          |
| sunbird\_cloud\_storage\_secret    | Player       |                      |                        |          |
| sunbird\_cloud\_report\_container  | Player       | reports              |                        |          |
| sunbird\_cloud\_storage\_region    | Player       |                      |                        |          |
| sunbird\_cloud\_storage\_container | Player       |                      |                        |          |
| sunbird\_gcloud\_project\_id       | Player       |                      |                        |          |

####

**Sample configuration for ED:**

```
sunbird_cloud_storage_key={{cloud_private_storage_accountname | default("")}}
sunbird_cloud_storage_secret={{cloud_private_storage_secret | default("")}}
sunbird_cloud_storage_container={{cloud_storage_public_bucketname | default("")}}
sunbird_cloud_report_container={{cloud_storage_privatereports_bucketname | default("reports")}}
sunbird_cloud_storage_region={{cloud_private_storage_region | default("")}}
sunbird_gcloud_project_id={{cloud_public_storage_project | default("")}
```

#### Jenkins Jobs:

| Service to be Build      | Build Tag          | Service to Deploy               | Deploy Tag                     | Comments |
| ------------------------ | ------------------ | ------------------------------- | ------------------------------ | -------- |
| Build/Kubernetes/Player  | release-5.1.0\_RC9 | Deploy/Kubernetes/Player        | release-5.1.0-vdn\_RC1         |          |
| Build/Kubernetes/Program | release-5.1.0\_RC1 | Deploy/Kubernetes/Program       | release-5.1.0-vdn\_RC1         |          |
|                          |                    | PostgresqlMigration             | sunbird-devops : release-5.1.0 |          |
|                          |                    | Deploy/Kubernetes/UploadSchemas | release-5.1.0\_RC4             |          |

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

