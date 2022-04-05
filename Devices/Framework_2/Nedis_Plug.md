## Tests
NOTE: Every criteria with the value of implementation as 'TODO' is not valued. The reasoning for this is either time, knowledge or equipment.

### A: Set up user and device
| nr| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| A.1 | The process is based on consent (GDPR 7) | 4 | 1 |
| A.2 | The user knows what they accepts, the possibility to know what consent means regarding the setup of the user | 4 | 1 |
| A.3 | Security-relevant user decision is covered by the documentation and a recommendation is given (ETSI 5.12) | 2 | 1 |
| A.4 | The default value for a decision follows best practice for security. (ETSI 5.12) | 2 | 2 |
| A.5 | Decision taken by the user is understandable for a user with limited technical knowledge (ETSI 5.12) | 2 | 1 |
| A.6 | Every decision taken by the user (prominently requested during setup) is necessary regarding the use of the device (ETSI 5.12) | 1 | 1 |
| A.7 | Device look for and initiate updates when first enabled if not latest version. | 3 | 1 |
| A.8 | Easy to use and read support material for users with limited technical knowledge. In addition the model designation shall be easy to find by several different methods, i.e. on the product itself, on the box it came in or the app (ETSI 5.3). | 2 | 1 |

### B1: Authentication 
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| B.1.1 | There is no indication that user input fields are vulnerable for injection-attacks and only users with right credentials are given proper access(ETSI 5.5) | 4 | 1 |
| B.1.2 | Every data input validation method is effective for validating the corresponding data input. The validation does not provide an indication that any data input does not protect against the processing of unexpected data inputs. ETSI 5.13 | 4 | 1 |
| B.1.3 | Log-in mechanism is protected from brute-force attacks by making it impractical to execute due to; <ul><li> time delay between failed attempts, or; </li><li>limited number of failed attempts, or; </li><li> Required two factor authentication. </li></ul> (ETSI 5.1) | 4 | 1|
| B.1.4 | Process for changing passwords is described in the privacy policy/user agreement and is easy to follow. The password is actually changed. (ETSI 5.1) | 4 | 1 |
| B.1.5 | Users must be authenticated towards the device to have access to its functionalities and interfaces. (ETSI 5.5) | 4 | 1 |
| B.1.6 | Password is recommended to be at least 8 characters and consists of at least one character from each character group. (big letters, small letters and numbers(special characters))  (ETSI 5.4) | 4 | 2 |
| B.1.7 | Administrator gets notifies about new/unauthorized changes in device software (ETSI 5.7) | 3 | 1 |
 
#### Reasoning for value of implementation

B.1.6: Two of the user decision had a default on. These were "Data analysis" and "Personalization". This is again not the most dangerous breaches, but can make the IoT devices slightly more vulnerable
### B2: Communication
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| B.2.1 | Communication of personal and sensitive data use best practice cryptographic.(ETSI 5.8) | 4 | 1|
| B.2.2 | All cryptographics detail are configured appropriately, is not known to be vulnerable and considered best practice(ETSI 5.1, 5.5, 5.8) | 4 | 1 |
| B.2.3 | The IoT-device can be isolated (ETSI 5.3) | 3 | 1 |
| B.2.4 | The level of security and mechanism used is appropriate for the use case of secure communication(ETSI 5.5) | 4 | 1|

### B3: Disclosing of vulnerability
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| B.3.1 | The Vulnerability disclosure policy of the company/organization is available for anybody/user, and contains contact information. (ETSI 5.2) | 4 | 1 |
| B.3.2 | The company/organization is also required to act upon vulnerabilities sent to the user contact in a timely manner (60-120 business days)(ETSI 5.2)  | 4 | TODO |

### C1: Default password
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| C.1.1 | Default password is generated uniquely per device. (ETSI 5.1) | 4 | 1 |
| C.1.2 | Default password does not make use of common patterns or common strings and is not related to public information. Password is recommended to be at least 8 characters and consists of at least one character from each character group. (big letters, small letters and numbers(special characters)) (ETSI 5.1) (ETSI 5.4) | 4 | 1 |



### C2: Erasure
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| C.2.1 | User have the right to require erasure of their personal data (GDPR 17) | 4 | 1 |
| C.2.2 | When a user requests erasure of data, third-parties of the company that have the data, will also erase the data.(GDPR 17) (ETSI 5.11) | 4 | TODO |
| C.2.3 | A clear confirmation is provided after deletions(ETSI 5.11) | 2 | TODO |
| C.2.4 | Users can make use of a simple functionality to erase their user data.(ETSI 5.11) | 4 | 1 |
| C.2.5 | Nothing indicates that the user data is not erased(ETSI 5.11) | 4 | TODO |
| C.2.6 | Privacy policy or user agreement covers how to erase, or delete personal data(ETSI 5.11) | 3 | 1 |

### C3: Personal data
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| C.3.1 | The user is able to edit and complete wrong and uncomplete data without undue delay (GDPR 16) | 4 | 1 |
| C.3.2 | All decisions about the user's personal data are based on consent.(GDPR 7) | 4 | 1 |
| C.3.3 | Users are able to withdraw their consent to use personal data and the processing of personal data at any time. And the process to withdraw is easy to find and understand.(GDPR 7)(ETSI 5.14) | 4 | 1|
| C.3.4 | The user has access to an easy to understand description about how personal data is being used, by whom, and for what purposes, as well as all processes their personal data may be used in.(ETSI 5.14) | 4 | 1 |
| C.3.5 | The user is informed about how to express consent (opt-in choice) to the different processes their personal data may be a part of.(ETSI 5.14) | 3 | 1 |
| C.3.6 | The user shall be provided with all the data the controller/company has of the user within one month from the receipt (GDPR 12) | 4 | 1 |
| C.3.7 | The users shall be informed if data is transferred to a third country or an international organization.(GDPR 15) | 4 | 1 |
| C.3.8 | Data collected is kept within the EU/EØS in countries that follow GDPR. | 2 | 2 |
| C.3.9 | Communication with the company is adequate for the request that is made. A confirmation of receival of a request is given. | 4 | 2 |
| C.3.10 | Privacy policy, user agreement and other relevant documentation is easy to find and contains all relevant information to the user. | 4 | 1 |

#### Reasoning for value of implementation

C.3.8: "Personal data may be transferred to other legal entities within the Datwyler Group located in countries inside and/or outside the European Union"
### D1: Updating and support
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| D.1.1 | Support period of the device is public available and a 5 years with updates after sale(Andrij) | 2 | 1|
| D.1.2 | The device looks for updates and initiate updates when first enabled if there is a new update (ETSI 5.3) | 3 | 1 |
| D.1.3 | Software updates are automatically and periodically checked and initiated. It is recommended to give the user the ability to manually check and install updates. (ETSI 5.3) | 4 | 1 |
| D.1.4 | The user is notified about critical security-updates (ETSI 5.3) | 2 | 1 |
| D.1.5 | The user is able to check the software version for the device (ETSI 5.3) | 2 | 1 |
| D.1.6 | Everything enabled by default is necessary for the device (ETSI 5.6) | 3 | 2 |
| D.1.7 | Every debug interface enabled is required, and can be disabled (ETSI 5.6) | 4 | 1 |

### D2: Physical
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| D.2.1 | Device is made by adequate physical material for its use case (Enisa) | 1 | 1 |
| D.2.1 | All exposed interfaces (Physical) are covered, protected or enabled as required, and accessible physical debug interfaces are disabled(ETSI 5.6) | 3 | 1 |

### E: Further tests that require specialized knowledge
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| E.1 | If the purpose for processing personal data is no longer valid, the controller shall stop processing of the data (GDPR 7) | 4 | TODO |
| E.2 | All measurement (telemetry) data is processing in the way the documentation describes (ETSI 5.14) | 4 | TODO |
| E.3 | Software security is appropriate for the task in regards to cryptography (ETSI 5.3) | 3 | TODO |
| E.4 | Update mechanism can not be misused (ETSI 5.3) | 4 | TODO |
| E.5 | The update mechanism is effective at verifying the authenticity of an update(ETSI 5.3) | 4 | TODO |
| E.6 | Passwords are stored according to the minimum required security practice.  | 4 | TODO |
| E.7 | Users have to be informed that any already processed/used personal data is still lawful, at the time withdrawal of consent is given.(GDPR 7) | 4 | TODO |
| E.8 | Hardcoded values are documented as such.(ETSI 5.4) | 1 | TODO |
| E.9 | Hardcoded values are protected by suitable mechanisms, including tamper-resistance(ETSI 5.4) | 3 | TODO |

## Risk matrix
In the matrix below have we just put the points that stands out, and where basic updates can be done: 
![image](https://user-images.githubusercontent.com/76153202/161737147-053776b3-4148-4263-9cce-4b3bc037e154.png)

