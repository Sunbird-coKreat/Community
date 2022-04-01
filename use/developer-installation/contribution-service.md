# Contribution Service

### System requirements

| Softwares / Frameworks | Version      |
| ---------------------- | ------------ |
| Node                   | 10x or above |
| Postgres               | 9.6          |
| Redis                  | 4.x or above |
| Kafka                  | 2.4.1        |

### Installation

The steps to install contribution/program service, are given in here.

{% embed url="https://github.com/Sunbird-Ed/program-service/tree/release-4.8.0#readme" %}

### Configuration

| S. NO. | VARIABLE NAME                           | DESCRIPTION                                                                    | PURPOSE                                                                           | DEFAULT                            |   |
| :----: | --------------------------------------- | ------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- | ---------------------------------- | - |
|    1   | dock\_base\_url                         | The co-kreat portal URL                                                        | To connect to the co-kreat portal                                                 | https://dockstaging.sunbirded.org  |   |
|    2   | sunbird\_base\_url                      | The sunbird portal URL                                                         | To connect to the sunbird portal                                                  | https://staging.sunbirded.org      |   |
|    3   | sunbird\_service\_log\_level            | Defines the log level                                                          | To define the log level                                                           | info                               |   |
|    4   | sunbird\_api\_auth\_token               | Represents the auth token to connect APIs                                      | To connect the services                                                           |                                    |   |
|    5   | learning\_service\_url                  | Learning service URL                                                           | Learning service URL                                                              | https://dock.sunbirded.org/action/ |   |
|    6   | learner\_service\_url                   | Learner Service URL                                                            | Learner Service URL                                                               |                                    |   |
|    7   | content\_service\_url                   | Content Service URL                                                            | Content Service URL                                                               | https://dock.sunbirded.org/action/ |   |
|    8   | opensaber\_service\_url                 | Contribution Registry URL                                                      | Contribution Registry URL                                                         |                                    |   |
|    9   | sunbird\_kafka\_host                    | Defines the Sunbird Kafka host                                                 | Used to connect to Kafka server                                                   |                                    |   |
|   10   | dock\_kafka\_host                       | Defines the Co-kreat Kafka host                                                | Used to connect to Kafka server                                                   |                                    |   |
|   11   | dock\_redis\_host                       | Defines the Redis server                                                       | Used to connect to Redis server                                                   |                                    |   |
|   12   | dock\_redis\_port                       | Defines the Redis server port                                                  |                                                                                   |                                    |   |
|   13   | sunbird\_question\_bulkupload\_topic    | Defines the default topic to be used for the content created using bulk upload | Represents the default topic to be used for the content created using bulk upload |                                    |   |
|   14   | sunbird\_assessment\_service\_base\_url | Assessment Service URL                                                         | Assessment Service URL                                                            |                                    |   |
|   15   | CORE\_INGRESS\_GATEWAY\_IP              | Ingress IP                                                                     | Ingress IP                                                                        |                                    |   |

