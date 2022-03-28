### Set up user
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| The process is based on consent (GDPR 7) | 4 | 1 |
| The user knows what they accepts, the possibility to know what consent means regarding the setup of the user | 4 | 1|
| Security-relevant user decision is covered by the documentation and a recommendation is given (ETSI 5.12) | 2 | 1 |
| Every data input validation method is effective for validating the corresponding data input. The validation does not provide an indication that any data input does not protect against the processing of unexpected data inputs. ETSI 5.13 | 4 | 1 |
| There is no indication that user input fields are vulnerable to injection-attacks and only users with right credentials are given proper access. (ETSI 5.5) | 4 | 1 |
| The default value for a decision follows best practice for security. (ETSI 5.12) | 2 |	4 |
| Decision taken by the user is understandable for a user with limited technical knowledge (ETSI 5.12) | 3 | 3 |
| Every decision taken by the user (prominently requested during setup) is necessary regarding the use of the device (ETSI 5.12) | 1 | 2 |

### Registration
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| Device look for and initiate updates when first enabled if not latest version. | 3 | 4 |
| Easy to use and read support material for users with limited technical knowledge. In addition the model designation shall be easy to find by several different methods, i.e. on the product itself, on the box it came in or the app (ETSI 5.3). | 2 | 1 |


### Authentication
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| Process for changing a password is described and easy to follow. A change of password is also actually made. (ETSI 5.1) | 4 | 1 |
| Log-in mechanism is protected from brute-force attacks by making it impractical to execute due to; <ul><li> time delay between failed attempts, or; </li><li>limited number of failed attempts, or; </li><li> Required two factor authentication. </li></ul> (ETSI 5.1) | 4 | 1 |
| Users must be authenticated towards the device to have access to its functionalities and interfaces. (ETSI 5.5) | 4 | 1 |
| Password is recommended to be at least 8 characters and consists of at least one character from each character group. (big letters, small letters and numbers(special characters))  (ETSI 5.4) | 4 | 1 |

 
### Defaults 
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| Default password is generated uniquely per device. (ETSI 5.1) | 4 | 1 |
| Default password does not make use of common patterns or common strings and is not related to public information.  Password is recommended to be at least 8 characters and consists of at least one character from each character group. (big letters, small letters and numbers(special characters)) (ETSI 5.1) (ETSI 5.4) | 4 | 1 |


### Updating
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| Support period of the device is publicly available. The device should be supported with updates for at least five years after the product has been sold. (ETSI 5.3) | 2 | 4 |
| Software updates are checked automatically and periodically, and can be initiated automatically. The user should be able to manually check and install updates. (ETSI 5.3) | 4 | TODO |
| User is notified about security-updates(ETSI 5.3) | 2 | Unknown |
| The user is able to check  the software version for the devis. | 2 | 1 |


### Security
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| Device is made of adequate physical material for its use case (enisa) | 1 | 1 |
| Communication of personal and sensitive data use best practice cryptographic.(ETSI 5.8) | 4 | 2 |
| All cryptographics detail are configured appropriately, is not known to be vulnerable and considered best practice(ETSI 5.1, 5.5, 5.8) | 4 | TODO |
| The DUT can be isolated (ETSI 5.3) | 3 | 1 |
| The level of security and mechanism used is appropriate for the use case of secure communication(ETSI 5.5) | 4 | 2 |
| User notification notify the administrator  about new/unauthorized changes in device software (ETSI 5.7) | 3 | 1 |

### Interfaces
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| Every debug interface enabled is required, and can be disabled (ETSI 5.6) | 4 | 1 |
| Everything enabled by default is necessary for the DUT (ETSI 5.6) | 3 | 1 |
| All exposed interfaces(physical) are covered, protected or enabled as required, and accessible physical debug interfaces are disabled (ETSI 5.6) | 3 | 1 |


### Erasure
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ---------- |
| User have the right to require erasure of their personal data (GDPR 17) | 4 | 1 |
| When a user requests erasure of data, third-parties of the company that have the data, will also erase the data.(GDPR 17) (ETSI 5.11) | 4 | 1 |
| A clear confirmation is provided after deletions(ETSI 5.11) | 2 | TODO |
| Users can make use of a simple functionality to erase their user data.(ETSI 5.11) | 4 | 1 |
| Nothing indicates that the user data is not erased(ETSI 5.11) | 4 | TODO |
| Privacy policy or user agreement covers how to erase, or delete personal data(ETSI 5.11) | 3 | 1 |


### Manipulation of data
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ---------- |
| The user is able to edit and complete uncompleted or wrong data without undue delay.(GDPR 16) | 4 | 1 |


### Personal data
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| All decisions about the user's personal data are based on consent.(GDPR 7) | 4 | 1 |
| Users are able to withdraw their consent to use personal data and the processing of personal data at any time. And the process to withdraw is easy to find and understand.(GDPR 7)(ETSI 5.14) | 4 | 1 |
| The user has access to an easy to understand description about how personal data is being used, by whom, and for what purposes, as well as all processes their personal data may be used in.(ETSI 5.14) | 4 | 1 |
| The user is informed about how to express consent (opt-in choice) to the different processes their personal data may be a part of.(ETSI 5.14) | 3 | 1 |
| The user shall be provided with all the data the controller/company has of the user within one month from the receipt (GDPR 12) | 4 | TODO |
| The users shall be informed if data is transferred to a third country or an international organization.(GDPR 15) | 4 | 1 |
| Data collected is kept within the EU in countries that follow GDPR. | 2 | TODO |


### Communication
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| Communication with the company is adequate for the request that is made.  A confirmation of receival of a request is given. | 4 | TODO |
| Privacy policy, user agreement and other relevant documentation is easy to find and contains all relevant information to the user. | 4 | TODO |


### Disclosing of vulnerability
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| The Vulnerability disclosure policy of the company/organization is available for anybody/user, and contains contact information. (ETSI 5.2) | 4 | 1 |
| The company/organization is also required to act upon vulnerabilities sent to the user contact in a timely manner (60-120 business days)(ETSI 5.2)  | 4 | TODO |

### Further tests that require specialized knowledge
| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- |
| If the purpose for processing personal data is no longer valid, then the controller/organization shall stop processing/usage of the data. (GDPR 11) | 4 | TODO |
| All measurements and data of that type is processing the way the documentation describes (ETSI 5.14) | 4 | TODO |
| Software security is appropriate for the task in regards to cryptography(ETSI 5.3) | 3 | TODO |
| Update mechanism cannot be misused(ETSI 5.3) | 4 | TODO |
| The update mechanism is effective at verifying the authenticity of an update(ETSI 5.3) | 4 | TODO |
| Passwords are stored according to the minimum required security practice. | 4 | |
| Users have to be informed that any already processed/used personal data is still lawful, at the time withdrawal of consent is given.(GDPR 7) | 4 | TODO |
| Hardcoded values are documented as such(ETSI 5.4) | 1 | |
| Hardcoded values are protected by suitable mechanisms, including tamper-resistance.(ETSI 5.4) | 3 | |

##Scoring
In the matrix show the points that can be improved
![image](https://user-images.githubusercontent.com/76153202/160400832-607f64da-d82c-4208-b633-80cd1764e522.png)


REASONING FOR VALUE OF IMPLEMENTATION:

SET6: Several options set to default for collection and access of data; Plan of product agreemnt; Other information about the status of the device.

SET7:  Certain explanations for options are not explained completely and in some cases not visible in the application.

SET8: User was in one case asked to allow access of usage of other apps

REG1:  No indication that device was updated when first configured TODO futher test to attempt update of device


UPD1:  No support period found

SEC2: Device make use of CoAP. Traffic does not seem to be encrypted, however it does not seem to be able to make use of the format. More research on CoAP protocol needed.

SEC5: CoAP is not the best encryption method, and has some known weaknesses
