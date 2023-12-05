# Components



Sunbird coKreat further consists of the following components:

## Reference coKreat web application <a href="#reference-cokreat-web-application" id="reference-cokreat-web-application"></a>

This is a reference web application that enables end to end workflows of the asset co-creation process. Please refer to [Co-creation Process section](https://project-sunbird.atlassian.net/wiki/spaces/SC/pages/3008692271) that details the workflows.

It consists of the front end code of the web application, including pages, widgets etc. It internally uses contribution service, contribution registry, sourcing data products and other Sunbird building blocks listed in the [Dependencies ](https://project-sunbird.atlassian.net/wiki/spaces/SC/pages/3008987139)section.

The the web application consists of the following two portals.

### a) Portal for sourcing organizations to source assets <a href="#portal-for-sourcing-organizations-to-source-assets" id="portal-for-sourcing-organizations-to-source-assets"></a>

This portal enables organizations to source assets, curate and publish them for consumption through sourcing projects. Following are the key features:

1. Create and publish a sourcing project with a defined scope of assets to be sourced and a schedule
2. Review the nominations to a sourcing project from contributors
3. Review the asset contributions to a sourcing project from the approved set of contributors
4. Curate and publish the assets for consumption

### b) Portal for contributors to contribute assets  <a href="#portal-for-contributors-to-contribute-assets" id="portal-for-contributors-to-contribute-assets"></a>

This portal enables contributors - individuals or organizations, to enroll as contributors and contribute assets for the various sourcing projects. Following are the key features:

1. Enroll as a contributor
2. Nominate to one or more sourcing projects
3. Contribute assets to the approved sourcing projects
4. Get the consumption details of the assets that got published for consumption

\<Today, the co-kreat BB makes an explicit call to the Sunbird Knowlg BB to push the asset in the consumption repo, which need to be modified to remove the underlying assumption that a consumption repo is always available.>

&#x20;

**code**: [GitHub - Sunbird-Ed/creation-portal: Web Portal for creating and curating content in Sunbird.](https://github.com/Sunbird-Ed/creation-portal)

## Contribution service <a href="#contribution-service" id="contribution-service"></a>

Contribution service is a micro-service to enable APIs to create and manage contribution projects, nominations and assigning users & roles for a project.\
**code**: [GitHub - Sunbird-Ed/program-service: Micro-service to create and manage programs, like a contribution program, etc.](https://github.com/Sunbird-Ed/program-service)

## Contributor registry <a href="#contributor-registry" id="contributor-registry"></a>

Contribution registry is a micro-service that is built on top of the v1 version of Sunbird RC(OpenSaber). It is used for managing contribution orgs, contribution org users and individual contributor profiles. Sunbird RC(OpenSaber) instance is configured with schemas for the entities - contributor org, contributor users and user-org association.

Though all contributors on coKreat platform are created as users using Sunbird Lern, this registry is required to store additional data about the contributors. This additional data comprises of contributor org or user preferences, contribution & org associations, summary data like content contribution counts, rewards & recognition data.

**code**: [GitHub - Sunbird-RC/open-saber at vidyadaan](https://github.com/Sunbird-RC/open-saber/tree/vidyadaan)

## Sourcing data products <a href="#sourcing-data-products" id="sourcing-data-products"></a>

We have below a list of data products in sourcing needs. Currently, it leverages Data Service from Sunbird Obsrv for this purpose. (It will be decoupled and moved as part of coKreat.)

1. **Collection Level gap report** - This report provides details of the number of assets(contents) that are linked to each collection and It helps project administrators track content availability vs. the needs at a collection level.
2. **Folder Level gap report** - This report provides details of the number of assets(contents) linked against each folder of the Collections. It helps project administrators track content availability vs. the needs at a chapter level.
3. **Visitor’s report** - This report provides details of the number of visitors to help you understand the traffic funnel and manage/expand the outreach campaign.
4. **Project level funnel report** - This report provides details of the number of visitors to help you understand the traffic funnel and manage/expand outreach campaign at a project level.
5. **Content details report** - This report provides details of all the assets(contents) that are contributed to across all projects. It helps administrators for multiple purposes like tracking the contribution or review status, as well as doing custom analysis related to the contributed content.
6. **Contribution usage metrics report** - This report provides details to the contributors on how many assets(contents) contributed are used, how much they are used(Usage details of the assets published).
