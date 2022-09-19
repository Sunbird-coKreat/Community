# Contribution Registry

Contribution registry stores the information about the individual contributors, organizations and the roles of various users in the organization. It also stores the metadata of the project scope.&#x20;

### **Contributor Organization**

When user enrolls as a **Contributor Organization**, Contribution Registry stores the User, Org and User\_Org Schemas.  User gets added as the organization admin, who has the privilege to invite other users to join this organization from contribution portal. These users can be called as Contributor Organization Users.

An Organization admin can:\
&#x20;\-  nominate their organization for contributing to a project\
&#x20;\-  invite users to contribute to their projects\
&#x20;\-  assign contributors or reviewers to their project\
&#x20;\-  review contributions done by contributors \
\
Users who accept the invite to join the organization to contribute content are given contributor roles within that organization. Admin can also grant 'Reviewer' roles to these contributors.&#x20;

### Individual Contributor

When a user enrolls as an **Individual Contributor**, only User schema is added to the Contribution Registry.&#x20;

An Individual Contributor can : \
&#x20;\- contribute the content by nominating to the respective project as an individual.\


![](<../../../.gitbook/assets/os\_search (1).png>)

### API documentation

Click [here](http://docs.sunbird.org/latest/apis/opensaber/) to know in detail about the APIs that power these workflows. &#x20;

### Schemas in the contribution Registry

#### User Schema :

User schema stores the information about User.  If the user is an individual contributor this schema has roles column set as \["individual"], for contributor Org Admin it is set to \["admin"], for and for a contributing Org User it is set to \["User"]. It also adds up all the mediums, subjects, and classes a user is contributing to and update those values here.&#x20;

| Key          | Value                                               |
| ------------ | --------------------------------------------------- |
| @type        | <mark style="color:orange;">User</mark>             |
| userId       | user identifier from the diksha profile of the User |
| firstName    | firstname from the diksha profile of the User       |
| lastName     | lastName from the diksha profile of the User        |
| channel      | Channel from the diksha profile of the User         |
| enrolledDate | Date of enrollment                                  |
| osid         | Unique Id given to the User in the registry         |
| roles        | \[]                                                 |
| gradeLevel   | \[]                                                 |
| medium       | \[]                                                 |
| subject      | \[]                                                 |

#### Org :&#x20;

Org schema stores the information about Contributing Organization, which is given by contributing Org Admin while enrolling.&#x20;

| Key         | Value                                            |
| ----------- | ------------------------------------------------ |
| @type       | <mark style="color:orange;">Org</mark>           |
| name        | Name of the Organization                         |
| description | Description of the Organization                  |
| code        | code generated from the name of the Organization |
| osid        | Unique Id given to the Org in the registry       |
| orgId       |                                                  |
| type        |                                                  |

#### User\_Org :

User\_Org schema stores the mapping of the user and Contributing Organization. The roles param decide whether the user is a normal contributing user or the admin of the Organization.

| Key    | Value                                                                                                                            |
| ------ | -------------------------------------------------------------------------------------------------------------------------------- |
| @type  | User\_Org                                                                                                                        |
| orgId  | osid of the Org                                                                                                                  |
| userId | osid of the User                                                                                                                 |
| roles  | <p>role user belongs to in the Org. can be one or many from ["admin" , "user" , <br> "sourcing_admin", "sourcing_reviewer"] </p> |
| osid   | Unique Id given to the User\_Org mapping in the registry                                                                         |

### Source code

{% embed url="https://github.com/Sunbird-RC/open-saber" %}

####

\
