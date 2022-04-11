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

![](../../.gitbook/assets/program\_service.jpg)

### Configuration

| S. NO. | VARIABLE NAME                           | DESCRIPTION                                                                    | PURPOSE                                                                           | DEFAULT                            |
| :----: | --------------------------------------- | ------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- | ---------------------------------- |
|    1   | dock\_base\_url                         | Represents the co-kreat portal URL                                             | To connect to the co-kreat portal                                                 | https://dockstaging.sunbirded.org  |
|    2   | sunbird\_base\_url                      | Represents the  sunbirdEd portal URL                                           | To connect to the sunbird portal                                                  | https://staging.sunbirded.org      |
|    3   | sunbird\_service\_log\_level            | Defines the log level                                                          | To define the log level                                                           | info                               |
|    4   | sunbird\_api\_auth\_token               | Represents the auth token to connect APIs                                      | To connect the services                                                           |                                    |
|    5   | learning\_service\_url                  | Represents the learning service URL                                            | To connect to the learning service URL                                            | https://dock.sunbirded.org/action/ |
|    6   | learner\_service\_url                   | Represents the learner service URL                                             | To connect to the learner service URL                                             |                                    |
|    7   | content\_service\_url                   | Represents the content service URL                                             | To connect to the content service URL                                             | https://dock.sunbirded.org/action/ |
|    8   | opensaber\_service\_url                 | Represents the contribution registry URL                                       | To connect to the contribution registry service URL                               |                                    |
|    9   | sunbird\_kafka\_host                    | Represents the sunbird Kafka host                                              | To connect to the Kafka server                                                    |                                    |
|   10   | dock\_kafka\_host                       | Represents the coKreat Kafka host                                              | To connect to the Kafka server                                                    |                                    |
|   11   | dock\_redis\_host                       | Represents the Redis server host                                               | To connect to the Redis server                                                    |                                    |
|   12   | dock\_redis\_port                       | Represents the Redis server port                                               |                                                                                   |                                    |
|   13   | sunbird\_question\_bulkupload\_topic    | Defines the default topic to be used for the content created using bulk upload | Represents the default topic to be used for the content created using bulk upload |                                    |
|   14   | sunbird\_assessment\_service\_base\_url | Represents the assessment service URL                                          | To connect to the assessment service URL                                          |                                    |
|   15   | CORE\_INGRESS\_GATEWAY\_IP              | Ingress IP                                                                     | Ingress IP                                                                        |                                    |

