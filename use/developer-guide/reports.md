# Reports

As part of coKreat we are having following list of Reports for Admin user in [sourcing portal](https://dockstaging.sunbirded.org/sourcing/orgreports).

Below are the list of reports that Admin user can see in sourcing portal

* Collection Level reports against the project/program (SourcingMetrics data)
* Folder level report against the project/program  (SourcingMetrics data)
* Visitors report&#x20;
* Project level report
* Content details report

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Sourcing portal reports</p></figcaption></figure>

### Github Repo for Sourcing Portal reports

{% embed url="https://github.com/Sunbird-Ed/sunbird-data-products/tree/5.1.0/data-products/src/main/scala/org/sunbird/analytics/sourcing" %}

Build & Deploy:\
\
Jenkins:[https://10.20.0.14/jenkins/job/Deploy/job/DockStaging/job/DataPipeline/](https://10.20.0.14/jenkins/job/Deploy/job/DockStaging/job/DataPipeline/)

{% embed url="https://github.com/Sunbird-Obsrv/sunbird-data-pipeline/blob/release-5.2.0/ansible/roles/data-products-deploy/templates/run-dock-job.j2" %}

{% embed url="https://github.com/Sunbird-Obsrv/sunbird-data-pipeline/blob/release-5.2.0/ansible/roles/data-products-deploy/templates/model-dock-config.j2" %}

DataSource -> vdn-content-model-snapshot in Druid

#### Video:

[View the introductory video here](https://drive.google.com/file/d/1g6f-ziir8MoK8RRLMcOT4psLz5PZflFK/view)

For more details about Hawk-eye/On-Demand reports refere the below Obsrv BB documentation

[https://obsrv.sunbird.org/previous-versions/sb-5.0-version/learn/product-and-developer-guide/report-configurator](https://obsrv.sunbird.org/previous-versions/sb-5.0-version/learn/product-and-developer-guide/report-configurator)

### Collection Level Content Gaps

This report details about rach collection (Course/Textbook etc) tagged to porgram, what are the different type of contents(by PrimaryCategory - number of contents) are attached to it.

It also shows number of folders present in the collection.

Sample report (data of CollectionLevel.csv file) looks like below

| Board   | Medium   | Grade   | Subject     | Collection Name | Total number of first level folders | Collection Category | Number of ClassroomTeachingVideo | Number of ConceptMap | Number of Course | Number of CuriosityQuestionSet | Number of ExperientialResource | Number of ExplanationReadingMaterial | Number of ExplanationResource | Number of ExplanationVideo | Number of FocusSpot | Number of LearningActivity | Number of LearningOutcomeDefinition | Number of LessonPlan | Number of LessonPlanResource | Number of LessonPlanUnit | Number of MarkingSchemeRubric | Number of OnboardingResource | Number of PedagogyFlow | Number of PracticeQuestionSet | Number of PracticeResource | Number of PreviousBoardExamPapers | Number of Resource | Number of SelfAssess | Number of TVLesson | Number of TeachingMethod | Number of TextBook | Number of eTextBook |
| ------- | -------- | ------- | ----------- | --------------- | ----------------------------------- | ------------------- | -------------------------------- | -------------------- | ---------------- | ------------------------------ | ------------------------------ | ------------------------------------ | ----------------------------- | -------------------------- | ------------------- | -------------------------- | ----------------------------------- | -------------------- | ---------------------------- | ------------------------ | ----------------------------- | ---------------------------- | ---------------------- | ----------------------------- | -------------------------- | --------------------------------- | ------------------ | -------------------- | ------------------ | ------------------------ | ------------------ | ------------------- |
| CBSE    | Assamese | KG      | Accountancy | 22.6.0 book     | 3                                   | Digital Textbook    | <p><br></p>                      | <p><br></p>          | <p><br></p>      | <p><br></p>                    | <p><br></p>                    | <p><br></p>                          | <p><br></p>                   | <p><br></p>                | <p><br></p>         | <p><br></p>                | <p><br></p>                         | <p><br></p>          | <p><br></p>                  | <p><br></p>              | <p><br></p>                   | <p><br></p>                  | <p><br></p>            | <p><br></p>                   | <p><br></p>                | <p><br></p>                       | 3                  | <p><br></p>          | <p><br></p>        | <p><br></p>              | <p><br></p>        | <p><br></p>         |
| unknown | Assamese | unknown | Biology     | NEW\_COURSE\_1  | 1                                   | Course              | <p><br></p>                      | <p><br></p>          | <p><br></p>      | <p><br></p>                    | <p><br></p>                    | <p><br></p>                          | <p><br></p>                   | <p><br></p>                | <p><br></p>         | <p><br></p>                | <p><br></p>                         | <p><br></p>          | <p><br></p>                  | <p><br></p>              | <p><br></p>                   | <p><br></p>                  | <p><br></p>            | <p><br></p>                   | <p><br></p>                | <p><br></p>                       | <p><br></p>        | 1                    | <p><br></p>        | <p><br></p>              | <p><br></p>        | <p><br></p>         |

### Folder Level(first Level) Content Gaps

This report give the details about each unit in the collection contains what type of contents and its count.

Sample report (data of FolderLevel.csv file) looks like below

| Board | Medium   | Grade | Subject     | Collection Name | Folder Name | Collection Category | Number of ClassroomTeachingVideo | Number of ConceptMap | Number of Course | Number of CuriosityQuestionSet | Number of ExperientialResource | Number of ExplanationReadingMaterial | Number of ExplanationResource | Number of ExplanationVideo | Number of FocusSpot | Number of LearningActivity | Number of LearningOutcomeDefinition | Number of LessonPlan | Number of LessonPlanResource | Number of LessonPlanUnit | Number of MarkingSchemeRubric | Number of OnboardingResource | Number of PedagogyFlow | Number of PracticeQuestionSet | Number of PracticeResource | Number of PreviousBoardExamPapers | Number of Resource | Number of SelfAssess | Number of TVLesson | Number of TeachingMethod | Number of TextBook | Number of eTextBook |
| ----- | -------- | ----- | ----------- | --------------- | ----------- | ------------------- | -------------------------------- | -------------------- | ---------------- | ------------------------------ | ------------------------------ | ------------------------------------ | ----------------------------- | -------------------------- | ------------------- | -------------------------- | ----------------------------------- | -------------------- | ---------------------------- | ------------------------ | ----------------------------- | ---------------------------- | ---------------------- | ----------------------------- | -------------------------- | --------------------------------- | ------------------ | -------------------- | ------------------ | ------------------------ | ------------------ | ------------------- |
| CBSE  | Assamese | KG    | Accountancy | 22.6.0 book     | Unit 1      | Digital Textbook    | <p><br></p>                      | <p><br></p>          | <p><br></p>      | <p><br></p>                    | <p><br></p>                    | <p><br></p>                          | <p><br></p>                   | <p><br></p>                | <p><br></p>         | <p><br></p>                | <p><br></p>                         | <p><br></p>          | <p><br></p>                  | <p><br></p>              | <p><br></p>                   | <p><br></p>                  | <p><br></p>            | <p><br></p>                   | <p><br></p>                | <p><br></p>                       | 1                  | <p><br></p>          | <p><br></p>        | <p><br></p>              | <p><br></p>        | <p><br></p>         |
| CBSE  | Assamese | KG    | Accountancy | 22.6.0 book     | Unit 2      | Digital Textbook    | <p><br></p>                      | <p><br></p>          | <p><br></p>      | <p><br></p>                    | <p><br></p>                    | <p><br></p>                          | <p><br></p>                   | <p><br></p>                | <p><br></p>         | <p><br></p>                | <p><br></p>                         | <p><br></p>          | <p><br></p>                  | <p><br></p>              | <p><br></p>                   | <p><br></p>                  | <p><br></p>            | <p><br></p>                   | <p><br></p>                | <p><br></p>                       | 1                  | <p><br></p>          | <p><br></p>        | <p><br></p>              | <p><br></p>        | <p><br></p>         |

### Visitors Report



### Project Level Report

This report shows number of contributions, rejections and approvals for the specific collection tagged to the program/project.

Sample report (data of FunnelReport.csv file) looks like below

| Report generation date | Project Name | No. of initiated nominations | No. of rejected nominations | No. of nominations pending review | No. of accepted nominations to the project | No. of contributors to the project | No. of contributions to the project | No. of contributions pending review | No. of approved contributions |
| ---------------------- | ------------ | ---------------------------- | --------------------------- | --------------------------------- | ------------------------------------------ | ---------------------------------- | ----------------------------------- | ----------------------------------- | ----------------------------- |
| 13-06-2022             | Test 1       | 0                            | 0                           | 0                                 | 1                                          | 0                                  | 0                                   | 0                                   | 0                             |
| 13-06-2022             | TN\_COURSE   | 1                            | 1                           | 0                                 | 2                                          | 1                                  | 10                                  | 10                                  | 0                             |
| 13-06-2022             | new12345667  | 0                            | 0                           | 0                                 | 2                                          | 0                                  | 0                                   | 0                                   | 0                             |

### Content Details Level Report

This report gives more details about each content tagged to the collection of the project/program.

This give more details about content metadata .

| Project Name | Project ID                           | Board              | Medium  | Grade   | Subject     | Object Type | Primary category | Collection/Question Set Name | Collection/Question Set ID | Folder ID                 | Content/Question Name | Content/Question ID       | Content Type     | MimeType        | Content/Question Status | Creator Name | CreatedBy ID                         | Topic   | Learning Outcome | Added from library |
| ------------ | ------------------------------------ | ------------------ | ------- | ------- | ----------- | ----------- | ---------------- | ---------------------------- | -------------------------- | ------------------------- | --------------------- | ------------------------- | ---------------- | --------------- | ----------------------- | ------------ | ------------------------------------ | ------- | ---------------- | ------------------ |
| SS0          | 9fad2bc0-fb6f-11eb-8b46-1744670276f3 | State (Tamil Nadu) | English | Class 2 | Mathematics | Collection  | Digital Textbook | 13AugRegionalUpload          | do\_213342918763905024153  | do\_213342918764683264158 | 2                     | do\_213342922509066240179 | Teacher Resource | video/webm      | Rejected                | vdn1         | c559b6da-8eba-45c8-8237-950b500f1f02 | unknown | unknown          | No                 |
| SS0          | 9fad2bc0-fb6f-11eb-8b46-1744670276f3 | State (Tamil Nadu) | English | Class 2 | Mathematics | Collection  | Digital Textbook | 13AugRegionalUpload          | do\_213342918763905024153  | do\_213342918764683264158 | 1                     | do\_213342922311704576178 | eTextbook        | application/pdf | Approved                | vdn1         | c559b6da-8eba-45c8-8237-950b500f1f02 | unknown | unknown          | No                 |

