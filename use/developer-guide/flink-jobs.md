# Flink Jobs

As part of coKreat deployment process, following jobs are built and deployed:

## content-auto-creator

Job playes vital role when\
\- Contents are uploaded in bulk\
\- single content is approved by sourcing org admin to make it available in consumption repo (i.e. Diksha)\
\- Bulk approval for contents is done by sourcing org admin to make the contents available in consumption repo (i.e. Diksha)

When contents are uploaded in bulk using CSV, `content/v4/import` API of coKreat infra is called, a corresponding event is generated and inserted into Kafka, which then triggers the content-auto-creator job. So the job has to be deployed on coKreat infra.\
\
When contents are to be make available in consumption repo, `content/v1/import` of consumption repo is called, a corresponding event is generated and inserted into Kafka, which then triggers the content-auto-creator job. So the job has to be available on consumption infra.\
\
Async operation is done by content-auto-creator job to ensure a seamless and efficient publishing process.\
&#x20;\
It ensures that published content is properly packaged, metadata is updated, indexing is efficient. Ultimately, the Job contributes to a robust and reliable publishing process within the system.  &#x20;

## auto-creator-v2

The Job is responsible to make question set(s) available on consumption repo.

Whenever an question set is approved or question sets are approved in bulk by sourcing org admin,  a corresponding event is generated and inserted into Kafka, which then triggers the `auto-creator-v2` job.

This job needs to available on consumption repo as questionset/v1/import of consumption repo is called to push question set over consumption repo.





Other Jobs used as we adopt other BBs

[content-publish: Knowlg](https://knowlg.sunbird.org/learn/product-and-developer-guide/content-service/content-apis/jobs/content-publish)

[Search Indexer: Knowlg](https://knowlg.sunbird.org/learn/product-and-developer-guide/assets-search-service/jobs/search-indexer)&#x20;

[asset-enrichment: Knowlg](https://knowlg.sunbird.org/learn/product-and-developer-guide/content-service/content-apis/jobs/asset-enrichment)

[async-questionset-publish](https://inquiry.sunbird.org/use/developer-installation/question-and-question-set-service/configuration#async-questionset-publish-flink-job)

##
