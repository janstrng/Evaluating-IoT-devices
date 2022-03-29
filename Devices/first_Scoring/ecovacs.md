# Framework test for Deebot 605

### Set up user

| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| Every decision taken by the user (prominently requested during setup) is necessary regarding the use of the device (ETSI 5.12) | 1 | 1 - User was in one case asked to allow access of usage of other apps. |
| The process is based on consent (GDPR 7) | 5 | 0 |
| The user knows what they accepts, the possibility to know what consent means regarding the setup of the user | 5 | 0 |
| The default value for a decision follows best practice for security. (ETSI 5.12) | 2 | 2 - Several options set to default for collection and access of data;  Plan of product agreemnt;  Other information about the status of the device. |
| Decision taken by the user is understandable for a user with limited technical knowledge (ETSI 5.12) | 3 | 2 - Certain explanations for options are not explained completely and in some cases not visible in the application. |
| Security-relevant user decision is covered by the documentation and a recommendation is given (ETSI 5.12) | 2 | 0 |
| There is no indication that user input fields are vulnerable to injection-attacks and only users with right credentials are given proper access. (ETSI 5.5) | 5 | 0 |
| Result: |  | 11/36 |

### Registration
| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| Device look for and initiate updates when first enabled if not latest version. | 4 | 2 - No indication that the device was updated when first configured.  TODO: further test to attempt update of device. |
| Easy to use and read support material for users with limited technical knowledge. In addition the model designation shall be easy to find by several different methods, i.e. on the product itself, on the box it came in or the app (ETSI 5.3). | 2 | 0 |
| Result: | | 8/12 |


### Authentication
| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| Process for changing a password is described and easy to follow. A change of password is also actually made. (ETSI 5.1) | 5 | 0 |
| Log-in mechanism is protected from brute-force attacks by making it impractical to execute due to; <ul><li> time delay between failed attempts, or; </li><li>limited number of failed attempts, or; </li><li> Required two factor authentication. </li></ul> (ETSI 5.1) | 5 | 0 |
| Passwords are stored according to the minimum required security practice. | 5 | TODO |
| Users must be authenticated towards the device to have access to its functionalities and interfaces. (ETSI 5.5) | 5 | 0 |
| Password is recommended to be at least 8 characters and consists of at least one character from each character group. (big letters, small letters and numbers(special characters))  (ETSI 5.4) | 5 | 0 |
| Result: | | 0/50 |
 
### Defaults 
| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| Default password is generated uniquely per device. (ETSI 5.1) | 5 | 0 |
| Default password does not make use of common patterns or common strings and is not related to public information.\n Password is recommended to be at least 8 characters and consists of at least one character from each character group. (big letters, small letters and numbers(special characters)) (ETSI 5.1) (ETSI 5.4) | 4 | 0 |
| Hardcoded values are documented as such and are protected by suitable mechanisms, including tamper-resistance. (ETSI 5.4) | 4 | 0 |
| Result: | | 0/26 |


### Updating
| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| Support period of the device is publicly available. The device should be supported with updates for at least five years after the product has been sold. (ETSI 5.3) | 2 | 2 - No support period found|
| Software updates are checked automatically and periodically, and can be initiated automatically. The user should be able to manually check and install updates. (ETSI 5.3) | 4 | TODO |
| User is notified about security-updates(ETSI 5.3) | 2 | Unknown |
| The user is able to check  the software version for the devis. | 2 | 0 |
| Result: | | 8/20 |


### Security
| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| Device is made of adequate physical material for its use case (enisa) | 1 | 0 |
| Communication of personal and sensitive data use best practice cryptographic.(ETSI 5.8) | 5 | 1 - Device make use of CoAP.  Traffic does not seem to be encrypted, however it does not seem to be able to make use of the format.  More research on CoAP protocol needed. |
| All cryptographics detail are configured appropriately, is not known to be vulnerable and considered best practice(ETSI 5.1, 5.5, 5.8) | 5 | TODO |
| Software security is appropriate for the task in regards to cryptography(ETSI 5.3) | 3 | TODO |
| Update mechanism cannot be misused(ETSI 5.3) | 4 | TODO |
| The update mechanism is effective at verifying the authenticity of an update(ETSI 5.3) | 4 | TODO |
| The DUT can be isolated (ETSI 5.3) | 3 | 0 |
| The level of security and mechanism used is appropriate for the use case of secure communication(ETSI 5.5) | 4 | 1 - TODO: look into vulnerabilities and weaknesses within CoAP. |
| User notification notify the administrator  about new/unauthorized changes in device software (ETSI 5.7) | 4 | 0 |
| Result: | | 9/48 |


### Interfaces
| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| Every debug interface enabled is required, and can be disabled (ETSI 5.6) | 4 | 0 |
| Everything enabled by default is necessary for the DUT (ETSI 5.6) | 4 | 0 |
| All exposed interfaces(physical) are covered, protected or enabled as required, and accessible physical debug interfaces are disabled (ETSI 5.6) | 3 | 0 |
| Result: | | 0/22 |


### Erasure
| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| User have the right to require erasure of their personal data (GDPR 17) | 5 | 0 |
| When a user requests erasure of data, third-parties of the company that have the data, will also erase the data.(GDPR 17) (ETSI 5.11) | 5 | 0 |
| A clear confirmation is provided after deletions(ETSI 5.11) | 4 | TODO |
| Users can make use of a simple functionality to erase their user data.(ETSI 5.11) | 4 | 0 |
| Nothing indicates that the user data is not erased(ETSI 5.11) | 4 | TODO |
| Privacy policy or user agreement covers how to erase, or delete personal data(ETSI 5.11) | 3 | 0 |
| Result: | | 0/40|


### Manipulation of data
| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| The user is able to edit and complete uncompleted or wrong data without undue delay.(GDPR 16) | 5 | 0 |
| Result: |  | 0/10 |

### Personal data
| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| All decisions about the user's personal data are based on consent.(GDPR 7) | 5 | 0 |
| Users are able to withdraw their consent to use personal data and the processing of personal data at any time. And the process to withdraw is easy to find and understand.(GDPR 7)(ETSI 5.14) | 5 | 0 |
| Users have to be informed that any already processed/used personal data is still lawful, at the time withdrawal of consent is given.(GDPR 7) | 5 | TODO |
| If the purpose for processing personal data is no longer valid, then the controller/organization shall stop processing/usage of the data. (GDPR 11) | 5 | TODO |
| The user has access to an easy to understand description about how personal data is being used, by whom, and for what purposes, as well as all processes their personal data may be used in.(ETSI 5.14) | 4 | 0 |
| The user is informed about how to express consent (opt-in choice) to the different processes their personal data may be a part of.(ETSI 5.14) | 4 | 0 |
| All measurements and data of that type is processed the way the documentation describes.(ETSI  5.14) | 4 | TODO |
| The user shall be provided with all the data the controller/company has of the user within one month from the receipt (GDPR 12) | 5 | TODO |
| The users shall be informed if data is transferred to a third country or an international organization.(GDPR 15) | 4 | 0 |
| Result: | | 0/82 |


### Disclosing of vulnerability
| Criterias | value of consequence | value of implementation |
| ----------- | ----------- | ----------- |
| The Vulnerability disclosure policy of the company/organization is available for anybody/user, and contains contact information. (ETSI 5.2) | 5 | 0 |
| The company/organization is also required to act upon vulnerabilities sent to the user contact in a timely manner (60-120 business days)(ETSI 5.2)  | 5 | TODO |
| Result: | | 0/20 |


## Score
with the use of the old scoring-system, Deebot got 32/366 points. -> score: 10/100
