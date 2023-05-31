# coKreat - Release v5.0.0

### Document release version <a href="#document-release-version" id="document-release-version"></a>

| Project | Release Date | Release Version |
| ------- | ------------ | --------------- |
| coKreat | 24-08-2022   | v5.0.0          |

### **Objectives of the coKreat release v5.0.0**

The Objective of coCkreat **5**.0.0 was to make coKreat platform adopter friendly by writing and improving documentation also as technical development, we have upgraded the cokreat portal's angular and node version.

### Scope

coKreat product release features and issues are described in this version 5.0.0. This document contains a short description of enhancements to the coKreat product.

### **Summary of the Product Features**

This document contains information on the following new features and enhancements to the existing features of the coKreat product

### **Description of the Product Features**

**Scope:** [**Link**](https://project-sunbird.atlassian.net/issues/?filter=12539)\*\*\*\*

| Sl.No | JIRA Id                                                           | Contributor | Jira issue Type | Description                                                                                  |
| ----- | ----------------------------------------------------------------- | ----------- | --------------- | -------------------------------------------------------------------------------------------- |
| **1** | [SB-30213](https://project-sunbird.atlassian.net/browse/SB-30213) | EkStep      | Story           | coKreat: Upgrade angular cli version to 10                                                   |
| 2     | [SB-30211](https://project-sunbird.atlassian.net/browse/SB-30211) | EkStep      | Story           | coKreat: Upgrade node version                                                                |
| 3     | [CO-7](https://project-sunbird.atlassian.net/browse/CO-7)         | EkStep      | Story           | Making Sunbird coKreat Cloud agnostic : Code changes to generalise CSP support               |
| 4     | [CO-61](https://project-sunbird.atlassian.net/browse/CO-61)       | Samagra     | RFC             | Editing of Questions during review of question by Question paper creator (Sourcing reviewer) |
| 5     | [CO-67](https://project-sunbird.atlassian.net/browse/CO-67)       | Samagra     | RFC             | Editing of Questions during review of question by Question paper creator                     |
| 6     | [CO-20](https://project-sunbird.atlassian.net/browse/CO-20)       | Samagra     | RFC             | Question Set Duplication                                                                     |
| 7     | [CO-18](https://project-sunbird.atlassian.net/browse/CO-18)       | Samagra     | RFC             | Question paper preview enabled before level-2 review                                         |
| 8     | [CO-19](https://project-sunbird.atlassian.net/browse/CO-19)       | Samagra     | RFC             | Quality check enabled for reviewers                                                          |
| 9     | [CO-17](https://project-sunbird.atlassian.net/browse/CO-17)       | Samagra     | RFC             | Question sets get removed when Project name is modified                                      |
| 10    | [CO-41](https://project-sunbird.atlassian.net/browse/CO-41)       | Samagra     | RFC             | User is able to submit MCQ questions for review without choosing correct answer              |

### **Test Scenarios:** [**Link**](https://project-sunbird.atlassian.net/wiki/spaces/COK/pages/3189997578/5.0.0+Cokreat+Test+Scenarios)

### **Upgrade to release-5.0.0**:



<table><thead><tr><th width="161">Variable Name</th><th width="144">Service Name</th><th width="196">Default Public Value</th><th width="126">Private Value Override</th><th width="189">Comments</th></tr></thead><tbody><tr><td>dock_interactive_video_qset_category</td><td>Player</td><td>Interactive Video Question Set</td><td></td><td>We need provide existing Question set primary categry name if we don't want to create new primary category for interactive video question set<br>Ex: Demo Practice Question Set</td></tr></tbody></table>

| Service to be Build               | Build Tag           | Service to Deploy                  | Deploy Tag             | Comments                                                          |
| --------------------------------- | ------------------- | ---------------------------------- | ---------------------- | ----------------------------------------------------------------- |
|                                   |                     |                                    |                        |                                                                   |
| Build/DataPipeline/EdDataProducts | release-5.0.0\_RC1  | Deploy/DataPipeline/EdDataProducts | release-5.0.0\_RC1     |                                                                   |
| Build/KnowledgePlatform/FlinkJobs | release-5.0.0\_RC3  | Deploy/KnowledgePlatform/FlinkJobs | release-5.0.0\_RC2     |                                                                   |
| Build/KnowledgePlatform/Learning  | release-5.0.0\_RC1  | Deploy/KnowledgePlatform/Learning  | release-5.0.0\_RC2     |                                                                   |
| Build/Kubernetes/Assessment       | release-5.0.0\_RC1  | Deploy/Kubernetes/Assessment       | release-5.0.0-vdn\_RC1 | code repo: https://github.com/Sunbird-inQuiry/inquiry-api-service |
| Build/Kubernetes/Content          | release-5.0.0\_RC1  | Deploy/Kubernetes/Content          | release-5.0.0-vdn\_RC1 |                                                                   |
| Build/Kubernetes/Player           | release-5.0.0\_RC13 | Deploy/Kubernetes/Player           | release-5.0.0-vdn\_RC1 |                                                                   |
| Build/Kubernetes/Search           | release-5.0.0\_RC1  | Deploy/Kubernetes/Search           | release-5.0.0-vdn\_RC1 |                                                                   |
| Build/Kubernetes/Taxonomy         | release-5.0.0\_RC1  | Deploy/Kubernetes/Taxonomy         | release-5.0.0-vdn\_RC1 |                                                                   |
|                                   |                     |                                    |                        |                                                                   |
|                                   |                     | Deploy/Kubernetes/OnboardAPIs      | release-5.0.0-vdn\_RC1 | Please deploy onboarding api job                                  |
|                                   |                     | Deploy/Kubernetes/UploadSchemas    | release-5.0.0-vdn\_RC1 |                                                                   |

#### Any Configurations OR Manual Steps OR Instructions - Please add here:

| Manual step                                                                                                                | Instruction                                           |
| -------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| Form config for                                                                                                            | https://project-sunbird.atlassian.net/browse/CO-18    |
| Form config for                                                                                                            | https://project-sunbird.atlassian.net/browse/CO-19    |
| Form config for                                                                                                            | https://project-sunbird.atlassian.net/browse/CO-67    |
| Form config for                                                                                                            | https://project-sunbird.atlassian.net/browse/CO-61    |
| Form config for                                                                                                            | https://project-sunbird.atlassian.net/browse/CO-18    |
| Form config for                                                                                                            | https://project-sunbird.atlassian.net/browse/CO-41    |
| Please create and add definition to the Interactive Video QuestionSet primary category from config mentioned in the ticket | https://project-sunbird.atlassian.net/browse/SB-30782 |
