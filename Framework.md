# Framework for cyberneticist- and privacy evaluation of IoT devices

## Background  
This framework is a part of a Bachelor thesis from NTNU and is based on criterias from "*[ETSI TS 103 701; Cyber Security for Consumer Internet of Things: Conformance Assessment of Baseline Requirements](https://www.etsi.org/deliver/etsi_ts/103700_103799/103701/01.01.01_60/ts_103701v010101p.pdf)*", criterias we found relevant from the *[General Data Protection Regulation (GDPR)](https://gdpr.eu/)* as well as "*[Enisa; Guidelines for securing the Internet of Things](https://www.enisa.europa.eu/publications/guidelines-for-securing-the-internet-of-things)*".  
## Scope of framework
The framework is a method to evaluate IoT devices aimed for stores providing the products to end-user, enthusiasts of security and private persons wanting to check their devices for security-flaws. The framework is therefore a high-level evaluation, utilizing free and available tools that can be used by people with limited (but some) technical knowledge.  

We have during development based the framework on devices with basic funcitonalities that is commonly found in households. These devices are commonly connected with Wifi and process data by communicating with an external server. The devices make use of and collect telemetric data from sensors such as thermometer, cameras, microphones and electric meter.

## Limitations
The framework is not a methodology of how to perform a penetration-test or find new vulnerabilities in IoT-devices. The main goal is to get an indication of how security has been taken into consideration in regards to the end-user by the provider. The framework does not replace GDPR or other requirements, but is a suggestion for users and vendors, with limited resources, of how to evaluate the security of an IoT-device with the use of publically available resources and tools.  
The framework does not include criteria for implementation of functionalities and will not make use of methods that require specialized knowledge such as code-reviewing and vulnerability-hunting/ research.
The main focus of the framework are for devices that primarily use Wifi as a method of communication, thus other protocols such as Zigbee and Z-wave have been left out of the scope.

## How to use
You use the framework by taking one device at a time and going through the points on the list below. You will most likely have to register an account on the corresponding app for the device, and this registration prosses is also a part of the evaluation. Some off the point may have a similar result, especially if the devices you test are from the same company/manufacturer and/or are using the same app. You can either download the file or you can print it out, and then fill in the “Value of implementation”, thereafter you fill in the score matrix.

## Definitions of Values

### Threat actors
![threatActorPyramid](https://user-images.githubusercontent.com/98017528/160378034-b47ff81d-0e7d-4f78-a7e0-0fda6a39c8bf.jpeg)  
Pyramid of threat actors[^1]

Defining and identifying the threat-actors we stand up against, we make use of the thret actor pyramid.  
The pyramid split the actors into six tiers.
- Tier 1: Script Kiddies and Non-Malicious actors;  
Have limited capabilities, tools, resources and knowledge. Techniques are usualy gathered from resources on the internet, and may therefore be able to use sophisticated tools to gain access.
- Tier 2: Criminals, Insider threats;  
Actor with a malicous motive to do damage. Mostly limited resorces and numbers, able to make use of known exploits and techniques.
- Tier 3: Crime groups and hacktivists;  
Actors that operate in groups and have access to unknown vulnerabilities and exploits. Often political motives or motives based on knowledge. Has resources to performe Distributed-Denial-of-Service.
- Tier 4: Organized Crime groups, Cyber Mercenaries;  
Actors with access to extensive tools and experience. Make use of actions such as ransomware or theft to achive profit. Targets big business-related information and documentation that could be of interest or be sold.
- Tier 5: State Sponsored;  
Advanced Persistent Threats that are sponsored by the state and therefore have access to and able to create advanced and sophisticated exploits and vulnerabilities. Usualy targets organization of strategic importance to gain personal and sensitive data.
- Tier 6: Nations;  
The most advanced threat-group. Offensive intelligence agencies of a country's cyber military. Capable of developing and creating new exploits and vulnerabilities with a specific target in mind. Often politicaly motivated and perform attacks to perform espionage, theft of intelectual property or political manipulation.

### Value of consequence (1-4)
1. The consequence will have little to no impact on the security of the user. It is not required for the device to make use of the criteria, and the device will not be considered unsafe for use. The user's rights to privacy will not be affected if the criteria is not implemented.
2. The consequences of deviation from the criterias are moderate. No implementation of the criteria could open the device up for potential attacks and loss of confidentiality and integrity. Consequence does not affect personal-data but could affect other types of data such as metrics.
The criteria makes a user friendly environment, where, if not fulfilled, can lead to some confusion between customer and the company.
3. Major consequences, The criteria is important for the device, but not critical. No implementation of the criteria could open up the device for potential attacks, loss of confidentiality and integrity.
A consequences of this would be personal data going astray
The criteria gives the user a friendly environment, where, if not fulfilled, can lead to confusion between customer and the company on security-related situations.
4. Critical consequences, this aspect of the device is considered unsafe if not implemented. The criteria is critical for the use, and security of the device and can not be in use before the criteria is used. No implementation could lead to all data going astray.

### Value of implementation (1-4)

The values of implementation indicate how the criteria has actually been taken into consideration and implemented into the product. This value will be used with the value of consequence to indicate how vulnerable the criteria is. The value also indicates the likeliness that the feature could be taken advantage of to achieve the level of consequence of the criteria.

1. Criteria has been taken into consideration and implemented with no indication that it does not follow best practice or with flaws. Likelihood that criteria is being misused to achieve consequence is very low and only actors with high motivation from tier 5 and 6 can successfully misuse the feature.
2. Criteria has been implemented with some flaws. Feature is not complete and is missing a core functionality or does not follow best practice. Likelihood of the criteria being misused to achieve consequence is low. The threat actor has to be in tier 3/4 or above to successfully misuse the feature with relative high motivation.
3. Criteria is barely taken into consideration and is implemented badly with many flaws. Likelihood of misusing the criteria is moderate. Likelihood of the criteria being misused to achieve consequence is moderate. The threat actor has to be in tier 2 or above and have some motivation to successfully misuse the feature.
4. Criteria has not been taken into consideration and is missing this feature. Likelihood of the criteria being misused to achieve consequence is high. The threat actor has to be in a tier in the pyramid to successfully misuse the feature with no defined motivation.


## Performing test
- A: Registration   
[A: Set up user and device](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#a-set-up-user-and-device)  
- B: Security  
[B1: Authentication](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#b1-authentication)  
[B2: Communication](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#b2-communication)  
[B3: Disclosing of vulnerability](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#b3-disclosing-of-vulnerability)  

- C: Data  
[C1: Default password](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#c1-default-password)  
[C2: Erasure](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#c2-erasure)  
[C3: Personal data](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#c3-personal-data)  
- D: Updates and interfaces  
[D1: Updating and support](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#d1-updating-and-support)  
[D2: Physical](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#d2-physical)  

- [E: Further tests](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#e-further-tests-that-require-specialized-knowledge)  

### A: Set up user and device
| Nr| Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| [A.1](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#a1-the-process-is-based-on-consent-gdpr-7) | The process is based on consent (GDPR 7) | 4 | |
| A.2 | The user knows what they accepts, the possibility to know what consent means regarding the setup of the user | 4 |  |
| A.3 | Security-relevant user decision is covered by the documentation and a recommendation is given (ETSI 5.12) | 2 |  |
| A.4 | The default value for a decision follows best practice for security. (ETSI 5.12) | 2 |  |
| A.5 | Decision taken by the user is understandable for a user with limited technical knowledge (ETSI 5.12) | 2 |  |
| A.6 | Every decision taken by the user (prominently requested during setup) is necessary regarding the use of the device (ETSI 5.12) | 1 |  |
| A.7 | Device look for and initiate updates when first enabled if not latest version. | 3 |  |
| A.8 | Easy to use and read support material for users with limited technical knowledge. In addition, the model designation shall be easy to find by several different methods, i.e. on the product itself, on the box it came in or the app (ETSI 5.3). | 2 |  |


### B1: Authentication 
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| [B.1.1](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#b11-and-b12-userdata-input-fields) | There is no indication that user input fields are vulnerable for injection-attacks and only users with right credentials are given proper access(ETSI 5.5) | 4 |  |
| [B.1.2](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#b11-and-b12-userdata-input-fields) | Every data input validation method is effective for validating the corresponding data input. The validation does not provide an indication that any data input does not protect against the processing of unexpected data inputs. ETSI 5.13 | 4 |  |
| B.1.3 | Log-in mechanism is protected from brute-force attacks by making it impractical to execute due to; <ul><li> time delay between failed attempts, or; </li><li>limited number of failed attempts, or; </li><li> Required two factor authentication. </li></ul> (ETSI 5.1) | 4 |  |
| B.1.4 | Process for changing passwords is described in the privacy policy/user agreement and is easy to follow. The password is actually changed. (ETSI 5.1) | 4 |  |
| B.1.5 | Users must be authenticated towards the device to have access to its functionalities and interfaces. (ETSI 5.5) | 4 |  |
| B.1.6 | Password is recommended to be at least 8 characters and consists of at least one character from each character group. (big letters, small letters and numbers)  (ETSI 5.4) | 4 |  |
| [B.1.7](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#b17-administratoruser-gets-notifies-about-newunauthorized-changes-in-device-software-etsi-57) | Administrator/user gets notifies about new/unauthorized changes in device software (ETSI 5.7) | 3 |  |
 
### B2: Communication 
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| B.2.1 | Communication of personal and sensitive data use best practice cryptographic.(ETSI 5.8) | 4 |  |
| B.2.2 | All cryptographic details are configured appropriately, is not known to be vulnerable and considered best practice(ETSI 5.1, 5.5, 5.8) | 4 |  |
| B.2.3 | The IoT-device can be isolated (ETSI 5.3) | 3 |  |
| B.2.4 | The level of security and mechanism used is appropriate for the use case of secure communication(ETSI 5.5) | 4 |  |


### B3: Disclosing of vulnerability
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| B.3.1 | The Vulnerability disclosure policy of the company/organization is available for anybody/user and contains contact information. (ETSI 5.2) | 4 |  |
| B.3.2 | The company/organization is also required to act upon vulnerabilities sent to the user contact in a timely manner (60-120 business days)(ETSI 5.2)  | 4 |  |

### C1: Default password
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| C.1.1 | Default password is generated uniquely per device. (ETSI 5.1) | 4 |  |
| C.1.2 | Default password does not make use of common patterns or common strings and is not related to public information. Password is recommended to be at least 8 characters and consists of at least one character from each character group. (big letters, small letters and numbers(special characters)) (ETSI 5.1) (ETSI 5.4) | 4 | |



### C2: Erasure
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| C.2.1 | User have the right to require erasure of their personal data (GDPR 17) | 4 |  |
| [C.2.2](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#c22-when-a-user-requests-erasure-of-data-third-parties-of-the-company-that-have-the-data-will-also-erase-the-datagdpr-17-etsi-511) | When a user requests erasure of data, third-parties of the company that have the data, will also erase the data.(GDPR 17) (ETSI 5.11) | 4 |  |
| C.2.3 | A clear confirmation is provided after deletions(ETSI 5.11) | 2 |  |
| C.2.4 | Users can make use of a simple functionality to erase their user data.(ETSI 5.11) | 4 |  |
| [C.2.5](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#c25-nothing-indicates-that-the-user-data-is-not-erased-etsi-511) | Nothing indicates that the user data is not erased(ETSI 5.11) | 4 |  |
| C.2.6 | Privacy policy or user agreement covers how to erase, or delete personal data(ETSI 5.11) | 3 |  |

### C3: Personal data
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| [C.3.1](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#c31-the-user-is-able-to-edit-and-complete-wrong-and-uncomplete-data-without-undue-delay-gdpr-16) | The user is able to edit and complete wrong and uncomplete data without undue delay (GDPR 16) | 4 |  |
| [C.3.2](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#c32-all-decisions-about-the-users-personal-data-are-based-on-consentgdpr-7) | All decisions about the user's personal data are based on consent.(GDPR 7) | 4 |  |
| [C.3.3](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#c33-users-are-able-to-withdraw-their-consent-to-use-personal-data-and-the-processing-of-personal-data-at-any-time-and-the-process-to-withdraw-is-easy-to-find-and-understandgdpr-7etsi-514) | Users are able to withdraw their consent to use personal data and the processing of personal data at any time. And the process to withdraw is easy to find and understand.(GDPR 7)(ETSI 5.14) | 4 |  |
| C.3.4 | The user has access to an easy to understand description about how personal data is being used, by whom, and for what purposes, as well as all processes their personal data may be used in.(ETSI 5.14) | 4 |  |
| [C.3.5](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#c35-the-user-is-informed-about-how-to-express-consent-opt-in-choice-to-the-different-processes-their-personal-data-may-be-a-part-of-etsi-514) | The user is informed about how to express consent (opt-in choice) to the different processes their personal data may be a part of.(ETSI 5.14) | 3 |  |
| [C.3.6](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#c36-the-user-shall-be-provided-with-all-the-data-the-controllercompany-has-of-the-user-within-one-month-from-the-receipt-gdpr-12) | The user shall be provided with all the data the controller/company has of the user within one month from the receipt (GDPR 12) | 4 |  |
| C.3.7 | The users shall be informed if data is transferred to a third country or an international organization.(GDPR 15) | 4 |  |
| C.3.8 | Data collected is kept within GDPR-compliant countries, and preferably within Europe. | 2 | |
| [C.3.9](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#c39-communication-with-the-company-is-adequate-for-the-request-that-is-made-a-confirmation-of-receival-of-a-request-is-given) | Communication with the company is adequate for the request that is made. A confirmation of receival of a request is given. | 4 | |
| C.3.10 | Privacy policy, user agreement and other relevant documentation is easy to find and contains all relevant information to the user. | 4 | |

### D1: Updating and support
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| D.1.1 | Support period of the device is public available and the device is updates in a auspicious time after the sale starts. | 2 |  |
| D.1.2 | The device looks for updates and initiate updates when first enabled if there is a new update (ETSI 5.3) | 3 |  |
| D.1.3 | Software updates are automatically and periodically checked and initiated. It is recommended to give the user the ability to manually check and install updates. (ETSI 5.3) | 4 |  |
| D.1.4 | The user is notified about critical security-updates (ETSI 5.3) | 2 |  |
| D.1.5 | The user is able to check the software version for the device (ETSI 5.3) | 2 |  |
| [D.1.6](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#d16-everything-enabled-by-default-is-necessary-for-the-device-etsi-56) | Everything enabled by default is necessary for the device (ETSI 5.6) | 3 |  |
| D.1.7 | Every debug interface enabled is required, and can be disabled (ETSI 5.6) | 4 |  |

### D2: Physical
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| [D.2.1](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#d21-device-is-made-by-adequate-physical-material-for-its-use-case-enisa) | Device is made by adequate physical material for its use case (Enisa) | 1 |  |
| [D.2.2](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Method.md#d22-all-exposed-interfaces-physical-are-covered-protected-or-enabled-as-required-and-accessible-physical-debug-interfaces-are-disabledetsi-56) | All exposed interfaces (Physical) are covered, protected or enabled as required, and accessible physical debug interfaces are disabled(ETSI 5.6) | 3 |  |

### E: Further tests that require specialized knowledge
| Nr | Criterias | Value of consequence | Value of implementation |
| ----------- | ----------- | ----------- | ----------- |
| E.1 | If the purpose for processing personal data is no longer valid, the controller shall stop processing of the data (GDPR 7) | 4 |  |
| E.2 | All measurement (telemetry) data is processing in the way the documentation describes (ETSI 5.14) | 4 |  |
| E.3 | Software security is appropriate for the task in regards to cryptography (ETSI 5.3) | 3 |  |
| E.4 | Update mechanism can not be misused (ETSI 5.3) | 4 |  |
| E.5 | The update mechanism is effective at verifying the authenticity of an update(ETSI 5.3) | 4 |  |
| E.6 | Passwords are stored according to the minimum required security practice.  | 4 |  |
| E.7 | Users have to be informed that any already processed/used personal data is still lawful, at the time withdrawal of consent is given.(GDPR 7) | 4 |  |
| E.8 | Hardcoded values are documented as such.(ETSI 5.4) | 1 |  |
| E.9 | Hardcoded values are protected by suitable mechanisms, including tamper-resistance(ETSI 5.4) | 3 |  |

 ### Reasoning for Value of implementation 
 
Under every table in the framework, you should put your reasoning for every criteria that do not have 1 as value of implementation. This will keep the tables clean and simple to read. You should put a reference to which criteria you are talking about. 
 <br>
 EXAMPLE:<br>
 B.1.6: Password only required 6 characters, with a combination of letters and number. With no requirement on big or small letters

## Scoring system

### Scoring system

The scoring system we choose to use for evaluating the IoT devices will be an qualitative risk matrix. There is a few reasons this is the this excact method of evaluting the results. Here are some important points with the risk matrix [^2] :
- The group have used the risk matrix multiple times earlier with success, and find it useless, and easy to use.
- The matrix identifies project risks
- The matrix shows, and identifies the risk criteria without any unnecessarily advanced methods
- Shows every identified risk criteria in a simple and understandable way 
- The group knows that the risk matrix is a subjective method of evaluation, because the implementer has to give a value that they feels is correct. Therefore every point should have an explenation on why they get the 'value of implementation.'
- With this method will the group be able to put in every point of the framework in to the matrix to see which point of the framework every device needs to improve. [^3] 
 
 
![image](https://user-images.githubusercontent.com/76153202/169229726-4ea577c0-ed62-4a36-9c78-ba3ef9d0b377.png)

For the scoring system have th egroup chosen 'value of consequence' * 'value of implmentation'. The conclution that have been made is that every score over 12 will be catergorized as 'RED', every score under 4 as 'GREEN', and every value between scores as 'Yellow'. A 'GREEN' score shows that there is a low value of risk for security, a 'YELLOW' score will have a medium risk of security, and a 'RED' score show a high risk of security.

Scoure:
[^1]: https://www.telenor.com/security-architecture-design-phase-the-concept-of-a-threat-intelligence-driven-defendable-architecture/

[^2]:  https://www.safran.com/content/introduction-qualitative-risk-analysis
 
[^3]: https://www.microtool.de/en/knowledge-base/what-is-a-risk-matrix/
