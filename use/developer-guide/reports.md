# Reports

### <mark style="color:blue;">**Hot-fix:  CSP**</mark>** (26-06-2024)**

| Component                                                              | Build Job                   | Build Tag                                                                                         | Deploy Job                                   | Deployment                                                                                           | Comment                                                                                                                                                                                                                                                                                                                                |
| ---------------------------------------------------------------------- | --------------------------- | ------------------------------------------------------------------------------------------------- | -------------------------------------------- | ---------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ETLJobs                                                                | Build/DataPipeline/ETLJobs  | [release-5.1.1\_RC1](https://github.com/Sunbird-Ed/sunbird-data-products/tree/release-5.1.1\_RC1) | Deploy/DataPipeline/ETLJobs                  | [release-5.2.0\_RC7](https://github.com/Sunbird-Obsrv/sunbird-data-pipeline/tree/release-5.2.0\_RC7) | <ul><li>script_to_run: DRUID_CONTENT_INDEXER</li><li>invoke_type: deploy</li></ul>                                                                                                                                                                                                                                                     |
| ETLDruidContentIndexer                                                 | NA                          | NA                                                                                                | Deploy/DataPipeline/ETLDruidContentIndexer   | [release-5.2.0\_RC7](https://github.com/Sunbird-Obsrv/sunbird-data-pipeline/tree/release-5.2.0\_RC7) | <ul><li>script_to_run: DRUID_CONTENT_INDEXER</li><li>invoke_type: execute-script</li></ul>                                                                                                                                                                                                                                             |
| Ed data product in dock env                                            | Build/Lern/LernDataProducts | [release-5.3.1\_RC11](https://github.com/Sunbird-Lern/data-products/tree/release-5.3.1\_RC11)     | Deploy/Dock/DataPipeline/EdDataProducts      | [release-5.3.1\_RC11](https://github.com/Sunbird-Lern/data-products/tree/release-5.3.1\_RC11)        | <p>CSP related changes.</p><ul><li>cloud_store_group_id: <strong>org.sunbird</strong></li><li>cloud_store_artifact_id: <strong>cloud-store-sdk_2.12</strong></li><li>cloud_store_version: <strong>1.4.6</strong></li></ul><p><strong>Note:</strong> While deploy select set the module value as <strong>dock-dataproducts</strong></p> |
| To run coKreat related report: Visitor's report                        | NA                          | NA                                                                                                | Deploy/DataPipeline/Runreport                | [release-5.2.0\_RC7](https://github.com/Sunbird-Obsrv/sunbird-data-pipeline/tree/release-5.2.0\_RC7) | report\_id: vidyadaan\_visitor                                                                                                                                                                                                                                                                                                         |
| To run coKreat related report: Collection Level Content Gaps           | NA                          | NA                                                                                                | Deploy/Dock/DataPipeline/AnalyticsReplayJobs | [release-5.3.1\_RC11](https://github.com/Sunbird-Lern/data-products/tree/release-5.3.1\_RC11)        | <ul><li><strong>job_type:</strong> run-job</li><li><strong>job_id:</strong> sourcing-metrics</li></ul>                                                                                                                                                                                                                                 |
| To run coKreat related report: Folder Level (first level) Content Gaps | NA                          | NA                                                                                                | Deploy/Dock/DataPipeline/AnalyticsReplayJobs | [release-5.3.1\_RC11](https://github.com/Sunbird-Lern/data-products/tree/release-5.3.1\_RC11)        | <ul><li><strong>job_type:</strong> run-job</li><li><strong>job_id:</strong> sourcing-metrics</li></ul>                                                                                                                                                                                                                                 |
| To run coKreat related report: Project level funnel report             | NA                          | NA                                                                                                | Deploy/Dock/DataPipeline/AnalyticsReplayJobs | [release-5.3.1\_RC11](https://github.com/Sunbird-Lern/data-products/tree/release-5.3.1\_RC11)        | <ul><li><strong>job_type: dock-</strong>run-job</li><li><strong>job_id:</strong> funnel-report</li></ul>                                                                                                                                                                                                                               |
| To run coKreat related report: Content Details Report                  | NA                          | NA                                                                                                | Deploy/Dock/DataPipeline/AnalyticsReplayJobs | [release-5.3.1\_RC11](https://github.com/Sunbird-Lern/data-products/tree/release-5.3.1\_RC11)        | <ul><li><strong>job_type: dock-</strong>run-job</li><li><strong>job_id:</strong> content-details</li></ul>                                                                                                                                                                                                                             |

As part of coKreat we are having following list of Reports for Admin user in [sourcing portal](https://dockstaging.sunbirded.org/sourcing/orgreports).

Below are the list of reports that Admin user can see in sourcing portal

* Collection Level reports against the project/program (SourcingMetrics data)
* Folder level report against the project/program  (SourcingMetrics data)
* Visitors report&#x20;
* Project level report
* Content details report

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Sourcing portal reports</p></figcaption></figure>

### Github Repo for Sourcing Portal reports

{% embed url="https://github.com/Sunbird-Lern/data-products/tree/release-5.3.1/lern-data-products/src/main/scala/org/sunbird/sourcing" %}

Build & Deploy:\
\
Jenkins:[https://10.20.0.14/jenkins/job/Deploy/job/DockStaging/job/DataPipeline/](https://10.20.0.14/jenkins/job/Deploy/job/DockStaging/job/DataPipeline/)

Jenkins deploy job: \
[http://150.230.132.241:8080/job/Deploy/job/dev/job/Lern/job/LernDataProducts/](http://150.230.132.241:8080/job/Deploy/job/dev/job/Lern/job/LernDataProducts/)\
\
Jenkins config change related job: [http://150.230.132.241:8080/job/Deploy/job/DockDev/job/DataPipeline/job/EdDataProducts/](http://150.230.132.241:8080/job/Deploy/job/DockDev/job/DataPipeline/job/EdDataProducts/)

Jenkins Analytics replay job: [http://150.230.132.241:8080/job/Deploy/job/DockDev/job/DataPipeline/job/AnalyticsReplayJobs/](http://150.230.132.241:8080/job/Deploy/job/DockDev/job/DataPipeline/job/AnalyticsReplayJobs/)

{% embed url="https://github.com/Sunbird-Lern/data-products/blob/release-5.3.1/ansible/roles/lern-data-products-deploy/templates/dock-run-job.j2" %}

{% embed url="https://github.com/Sunbird-Lern/data-products/blob/release-5.3.1/ansible/roles/lern-data-products-deploy/templates/dock-model-config.j2" %}

#### DataSource( In Druid)

We have to configure the datasource in druid to index all the required fields for the sourcing admin-reports. Find the below details of Druid datasource.

**DataSource - vdn-content-model-snapshot**

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

The above datasource is used to generate the admin reports(.csv) file for the below list of reports

* Collection Level reports against the project/program (SourcingMetrics data)
* Folder level report against the project/program  (SourcingMetrics data)
* Project level report
* Content details report

Druid Datasource Settings

Add the following JSON configuration to set up your Druid datasource:

```json
{
    "binaryVersion": 9,
    "dataSource": "vdn-content-model-snapshot",
    "dimensions": "author,board,lastStatusChangedOn,collectionId,organisationId,acceptedContents,acceptedContributions,rejectedContents,rejectedContributions,chapterCount,mvcContentCount,sampleContent,unitIdentifiers,channel,originData,compatibilityLevel,contentType,createdBy,createdFor,createdOn,creator,framework,gradeLevel,identifier,keywords,language,lastPublishedBy,lastPublishedOn,lastSubmittedOn,lastUpdatedBy,lastUpdatedOn,license,mediaType,medium,mimeType,name,objectType,organisation,origin,owner,pkgVersion,resourceType,status,prevStatus,primaryCategory,subject,topic,version,programId,type,category,learningOutcome,qumlVersion,bloomsLevel,rejectComment,reusedContributions",
    "identifier": "vdn-content-model-snapshot_2023-06-13T00:00:00.000Z_2023-06-14T00:00:00.000Z_2023-06-13T17:05:36.968Z",
    "interval": "2023-06-13T00:00:00.000Z/2023-06-14T00:00:00.000Z",
    "loadSpec": {
        "blobPath": "vdn-content-model-snapshot/20230613T000000.000Z_20230614T000000.000Z/2023-06-13T17_05_36.968Z/0/index.zip",
        "containerName": "telemetry-data-store",
        "type": "azure"
    },
    "metrics": "me_audiosCount,me_averageInteractionsPerMin,me_averageRating,me_totalTimeSpentInPortal,me_totalTimeSpentInApp,me_totalTimeSpentInDesktop,me_totalPlaySessionCountInApp,me_totalPlaySessionCountInDesktop,me_totalPlaySessionCountInPortal,me_averageSessionsPerDevice,me_averageTimespentPerSession,me_avgCreationTsPerSession,me_creationSessions,me_creationTimespent,me_hierarchyLevel,me_imagesCount,me_timespentDraft,me_timespentReview,me_totalComments,me_totalDevices,me_totalDialcodeAttached,me_totalDialcodeLinkedToContent,me_totalDownloads,me_totalInteractions,me_totalRatings,me_totalSessionsCount,me_totalSideloads,me_totalTimespent,me_videosCount",
    "shardSpec": {
        "partitionNum": 0,
        "partitions": 0,
        "type": "numbered"
    },
    "size": 64465556,
    "version": "2023-06-13T17:05:36.968Z"
}
```

This configuration ensures the proper collection and indexing of the specified datasource fields for analysis.

#### **"Visitors report" Configuration**

For "Visitors report" we have to configure the report using "ReportConfigure" API. The \`reportId\`  is the key to identify the visitors report is configured or not&#x20;

`"reportId": "vidyadaan_visitor"`

API -&#x20;

<pre class="language-powershell"><code class="lang-powershell"><strong>{{host}}api/data/v1/report/jobs/vidyadaan_visitor
</strong></code></pre>

body:

```json
{
        "reportId": "vidyadaan_visitor",
        "config": {
            "reportConfig": {
                "id": "vidyadaan_visitor",
                "mergeConfig": {
                    "rollupRange": 30,
                    "rollupAge": "DAY",
                    "postContainer": "reports",
                    "container": "reports",
                    "basePath": "/mount/data/analytics/tmp",
                    "reportPath": "vidyadaan_visitor.csv",
                    "rollupCol": "Date||%d-%m-%Y",
                    "frequency": "DAILY",
                    "rollup": 1
                },
                "labels": {
                    "state": "Channel",
                    "legend": "Visitors Count",
                    "context_channel_slug": "Channel",
                    "total_content_plays_on_portal": "No of Visitors",
                    "total_count": "total_content_plays_on_portal"
                },
                "dateRange": {
                    "staticInterval": "LastDay",
                    "granularity": "day",
                    "intervalSlider": 0
                },
                "metrics": [
                    {
                        "metric": "total_content_plays_on_portal",
                        "label": "total_content_plays_on_portal",
                        "druidQuery": {
                            "dataSource": "telemetry-events-syncts",
                            "filters": [
                                {
                                    "type": "equals",
                                    "dimension": "edata_pageid",
                                    "value": "contribution_all_projects"
                                },
                                {
                                    "type": "equals",
                                    "dimension": "eid",
                                    "value": "IMPRESSION"
                                },
                                {
                                    "type": "equals",
                                    "dimension": "context_pdata_id",
                                    "value": "prod.vidyadaan.portal"
                                }
                            ],
                            "threshold": 10000,
                            "granularity": "day",
                            "dimensions": [
                                {
                                    "fieldName": "context_channel",
                                    "outputName": "context_channel_slug",
                                    "extractionFn": [
                                        {
                                            "type": "registeredLookup",
                                            "retainMissingValue": true,
                                            "fn": "channelSlugLookup"
                                        }
                                    ],
                                    "type": "extraction",
                                    "aliasName": "context_channel_slug"
                                }
                            ],
                            "aggregations": [
                                {
                                    "name": "total_content_plays_on_portal",
                                    "type": "count",
                                    "fieldName": "count"
                                }
                            ],
                            "postAggregations": [],
                            "queryType": "groupBy"
                        }
                    }
                ],
                "output": [
                    {
                        "type": "csv",
                        "metrics": [
                            "total_content_plays_on_portal"
                        ],
                        "dims": [
                            "context_channel_slug",
                            "date"
                        ],
                        "fileParameters": [
                            "id",
                            "dims"
                        ]
                    }
                ],
                "queryType": "groupBy"
            },
            "store": "azure",
            "container": "reports",
            "key": "hawk-eye/"
        },
        "requestedBy": "analytics",
        "reportDescription": "vidyadaan_visitor_report",
        "status": "ACTIVE",
        "status_msg": "REPORT SUCCESSFULLY ACTIVATED",
        "reportSchedule": "Daily"
    }
```

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

Sample report (data of VisitorsReport.csv file) looks like below

| Date       | Channel | No of Visitors |
| ---------- | ------- | -------------- |
| 18-07-2022 | ekstep  | 7              |
| 19-07-2022 | ekstep  | 1              |
| 20-07-2022 | ekstep  | 9              |

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
