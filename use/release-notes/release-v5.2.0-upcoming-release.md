# Release v5.2.0 (Upcoming release)

### Document release version <a href="#document-release-version" id="document-release-version"></a>

| Project | Release Date | Version |
| ------- | ------------ | ------- |
| cokreat |              |         |

### **Objectives of the coKreat release v5.2.0**

The Objective of coCkreat **5.120** aims at fixing the known bugs for the release and make the cokreat portal as cloud agnostic.

### Scope:

coKreat product release features and issues are described in this version 5.1.0. This document contains a short description of bugs to the coKreat product.

### **Summary of the Product Features:**

This document contains information on the following existing bugs of the coKreat product

### **Description of the Product Features**

**Ekstep Contributor Scope:**

**Samagra Contributor Scope:**&#x20;

| Sl.no | JIRA Id | Contributor | Issue Type        | Description |
| ----- | ------- | ----------- | ----------------- | ----------- |
| 1     |         | Ekstep      | Minor Enhancement |             |
| 2     |         | Ekstep      | Bug               |             |

### **Ekstep Contribution Test Scenarios:**&#x20;

### **Samagra Contribution Test Case:**&#x20;

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

<mark style="color:red;"></mark>

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



