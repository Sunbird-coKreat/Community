# Asset Sourcing

Asset sourcing capability is enabled by the following components of coKreat building block.

### 1) Reference coKreat web application <a href="#reference-cokreat-web-application" id="reference-cokreat-web-application"></a>

It consists of the front end code of the web application, including pages, widgets etc. It internally uses contribution service, contribution registry, sourcing data products and other Sunbird building blocks.

The web application consists of the following two portals.

#### a) Portal for sourcing organizations to source assets <a href="#portal-for-sourcing-organizations-to-source-assets" id="portal-for-sourcing-organizations-to-source-assets"></a>

This portal enables organizations to source assets, curate and publish them for consumption through sourcing projects. Following are the key features:

1. Create and publish a sourcing project with a defined scope of assets to be sourced and a schedule
2. Review the nominations to a sourcing project from contributors
3. Review the asset contributions to a sourcing project from the approved set of contributors
4. Curate and publish the assets for consumption

#### b) Portal for contributors to contribute assets  <a href="#portal-for-contributors-to-contribute-assets" id="portal-for-contributors-to-contribute-assets"></a>

This portal enables contributors - individuals or organizations, to enroll as contributors and contribute assets for the various sourcing projects. Following are the key features:

1. Enroll as a contributor
2. Nominate to one or more sourcing projects
3. Contribute assets to the approved sourcing projects
4. Get the consumption details of the assets that got published for consumption

### 2) Contribution Service

Contribution service consists of APIs to create and manage contribution projects, nominations and assigning users & roles for a project.

### 3) Contribution Registry

Contribution registry consists of APIs to manage contribution orgs, contribution org users and individual contributor profiles.&#x20;

### 4) Data Products

coKreat provides six out of the box reports which help sourcing organization administrators to gauze the health of the sourcing projects and intervene, when needed.&#x20;

1. **Collection Level gap report** - This report provides details of the number of assets(content) that are linked to each collection and It helps project administrators track content availability vs. the needs at a collection level.
2. **Folder Level gap report** - This report provides details of the number of assets(content) linked against each folder of the Collections. It helps project administrators track content availability vs. the needs at a chapter level.
3. **Visitor’s report** - This report provides details of the number of visitors to help you understand the traffic funnel and manage/expand the outreach campaign.
4. **Project level funnel report** - This report provides details of the number of visitors to help you understand the traffic funnel and manage/expand outreach campaign at a project level.
5. **Content details report** - This report provides details of all the assets(contents) that are contributed to across all projects. It helps administrators for multiple purposes like tracking the contribution or review status, as well as doing custom analysis related to the contributed content.
6. **Contribution usage metrics report** - This report provides details to the contributors on how many assets(contents) contributed are used, how much they are used(Usage details of the assets published).

