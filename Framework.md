# Framework for evaluating IoT-devices

## Scope of framework
The framework does not depict a methodology of how to performe a penetration-test or find new vulnerabilities in IoT-devices. The main goal is to get an indication of how security has been taken into consideration in regards to the end-user by the provider. The framework does not replace GDPR or other requirements, but is a suggestion for users and vendors, with limited resources, of how to evaluate the security of an IoT-device with the use of open source resources and tools.

## Limitations
The framework does not include criteria for implementation of functionalities and will not make use of methods that require specialized knowledge such as code-reviewing and vulnerability-hunting/ research.
The main focus of the framework are for devices that primarily use Wifi as a method of communication, thus other protocols such as Zigbee and Z-wave have been left out of the scope.

## Definitions of Values

### Value of consequence (1-5)
1. The consequence will have little to no impact on the security of the user. It is not required for the device to make use of the criteria, and the device will not be considered unsafe for use. The user's rights to privacy will not be affected if the criteria is not implemented.
2. The consequence will have some impact to the security of the user and the users rights to privacy may be affected if the criteria is not implemented. It is recommended but not required for the device to make use of the criteria.
3. The consequences of deviation from the criterias are moderate. No implementation of the criteria could open the device up for potential attacks and loss of confidentiality and integrity. Consequence does not affect personal-data but could affect other types of data such as metrics.
The criteria makes a user friendly environment, where, if not fulfilled, can lead to confusion between customer and the company.
4. Bad consequences, The criteria is important for the device, but not critical. No implementation of the criteria could open up the device for potential attacks, loss of confidentiality and integrity. A consequences of this would be personal data going astray.
The criteria makes a user friendly environment, where, if not fulfilled, can lead to confusion between customer and the company on security-related situations
5. Critical consequences, this aspect of the device is considered unsafe if not implemented. The criteria is critical for the use, and security of the device and can not be in use before the criteria is used. No implementation of criteria could lead to all data going astray.

### Value of implementation (0-2)

The values of implementation indicate how the criteria has actually been taken into consideration and implemented into the product. This value will be used with the value of consequence to indicate how vulnerable the criteria is.

0. Criteria has been taken into consideration and implemented with no indication that it does not follow best practice or with flaws.
1. Criteria has been implemented with flaws. Feature is not complete and is missing a core functionality or does not follow best practice.
2. Criteria has not been taken into consideration and is missing this feature or has been implemented badly to an extent that it does not fulfill its function.

## Tests
### Set up user
| Criterias | Value of consequence |
| ----------- | ----------- |
| The process is based on consent (GDPR 7) | 5 |
| The user knows what they accepts, the possibility to know what consent means regarding the setup of the user | 5 |
| Security-relevant user decision is covered by the documentation and a recommendation is given (ETSI 5.12) | 2 |
| Every data input validation method is effective for validating the corresponding data input. The validation does not provide an indication that any data input does not protect against the processing of unexpected data inputs. ETSI 5.13 | 4 |
| There is no indication that user input fields are vulnerable to injection-attacks and only users with right credentials are given proper access. (ETSI 5.5) | 5 |
| The default value for a decision follows best practice for security. (ETSI 5.12) | 2 |
| Decision taken by the user is understandable for a user with limited technical knowledge (ETSI 5.12) | 3 |
| Every decision taken by the user (prominently requested during setup) is necessary regarding the use of the device (ETSI 5.12) | 1 |

### Registration
| Criterias | Value of consequence |
| ----------- | ----------- |
| Device look for and initiate updates when first enabled if not latest version. | 4 |
| Easy to use and read support material for users with limited technical knowledge. In addition the model designation shall be easy to find by several different methods, i.e. on the product itself, on the box it came in or the app (ETSI 5.3). | 2 |


### Authentication
| Criterias | Value of consequence |
| ----------- | ----------- |
| Process for changing a password is described and easy to follow. A change of password is also actually made. (ETSI 5.1) | 5 |
| Log-in mechanism is protected from brute-force attacks by making it impractical to execute due to; <ul><li> time delay between failed attempts, or; </li><li>limited number of failed attempts, or; </li><li> Required two factor authentication. </li></ul> (ETSI 5.1) | 5 |
| Users must be authenticated towards the device to have access to its functionalities and interfaces. (ETSI 5.5) | 5 |
| Password is recommended to be at least 8 characters and consists of at least one character from each character group. (big letters, small letters and numbers(special characters))  (ETSI 5.4) | 5 |

 
### Defaults 
| Criterias | Value of consequence |
| ----------- | ----------- |
| Default password is generated uniquely per device. (ETSI 5.1) | 5 |
| Default password does not make use of common patterns or common strings and is not related to public information.\n Password is recommended to be at least 8 characters and consists of at least one character from each character group. (big letters, small letters and numbers(special characters)) (ETSI 5.1) (ETSI 5.4) | 4 |


### Updating
| Criterias | Value of consequence |
| ----------- | ----------- |
| Support period of the device is publicly available. The device should be supported with updates for at least five years after the product has been sold. (ETSI 5.3) | 2 |
| Software updates are checked automatically and periodically, and can be initiated automatically. The user should be able to manually check and install updates. (ETSI 5.3) | 4 |
| User is notified about security-updates(ETSI 5.3) | 2 |
| The user is able to check  the software version for the devis. | 2 |


### Security
| Criterias | Value of consequence |
| ----------- | ----------- |
| Device is made of adequate physical material for its use case (enisa) | 1 |
| Communication of personal and sensitive data use best practice cryptographic.(ETSI 5.8) | 5 |
| All cryptographics detail are configured appropriately, is not known to be vulnerable and considered best practice(ETSI 5.1, 5.5, 5.8) | 5 |
| The DUT can be isolated (ETSI 5.3) | 3 |
| The level of security and mechanism used is appropriate for the use case of secure communication(ETSI 5.5) | 4 |
| User notification notify the administrator  about new/unauthorized changes in device software (ETSI 5.7) | 4 |

### Interfaces
| Criterias | Value of consequence |
| ----------- | ----------- |
| Every debug interface enabled is required, and can be disabled (ETSI 5.6) | 4 |
| Everything enabled by default is necessary for the DUT (ETSI 5.6) | 4 |
| All exposed interfaces(physical) are covered, protected or enabled as required, and accessible physical debug interfaces are disabled (ETSI 5.6) | 3 |


### Erasure
| Criterias | Value of consequence |
| ----------- | ----------- |
| User have the right to require erasure of their personal data (GDPR 17) | 5 |
| When a user requests erasure of data, third-parties of the company that have the data, will also erase the data.(GDPR 17) (ETSI 5.11) | 5 |
| A clear confirmation is provided after deletions(ETSI 5.11) | 4 |
| Users can make use of a simple functionality to erase their user data.(ETSI 5.11) | 4 |
| Nothing indicates that the user data is not erased(ETSI 5.11) | 4 |
| Privacy policy or user agreement covers how to erase, or delete personal data(ETSI 5.11) | 3 |


### Manipulation of data
| Criterias | Value of consequence |
| ----------- | ----------- |
| The user is able to edit and complete uncompleted or wrong data without undue delay.(GDPR 16) | 5 |


### Personal data
| Criterias | Value of consequence |
| ----------- | ----------- |
| All decisions about the user's personal data are based on consent.(GDPR 7) | 5 |
| Users are able to withdraw their consent to use personal data and the processing of personal data at any time. And the process to withdraw is easy to find and understand.(GDPR 7)(ETSI 5.14) | 5 |
| Users have to be informed that any already processed/used personal data is still lawful, at the time withdrawal of consent is given.(GDPR 7) | 5 |
| The user has access to an easy to understand description about how personal data is being used, by whom, and for what purposes, as well as all processes their personal data may be used in.(ETSI 5.14) | 4 |
| The user is informed about how to express consent (opt-in choice) to the different processes their personal data may be a part of.(ETSI 5.14) | 4 |
| The user shall be provided with all the data the controller/company has of the user within one month from the receipt (GDPR 12) | 5 |
| The users shall be informed if data is transferred to a third country or an international organization.(GDPR 15) | 4 |
| Data collected is kept within the EU in countries that follow GDPR. | 3 |


### Communication
| Criterias | Value of consequence |
| ----------- | ----------- |
| Communication with the company is adequate for the request that is made.  A confirmation of receival of a request is given within a week. | 5 |
| Privacy policy, user agreement and other relevant documentation is easy to find and contains all relevant information to the user. | 5 |


### Disclosing of vulnerability
| Criterias | Value of consequence |
| ----------- | ----------- |
| The Vulnerability disclosure policy of the company/organization is available for anybody/user, and contains contact information. (ETSI 5.2) | 5 |
| The company/organization is also required to act upon vulnerabilities sent to the user contact in a timely manner (60-120 business days)(ETSI 5.2)  | 5 |

### Further tests that require specialized knowledge
| Criterias | Value of consequence |
| ----------- | ----------- |
| If the purpose for processing personal data is no longer valid, then the controller/organization shall stop processing/usage of the data. (GDPR 11) | 5 |
| All measurements and data of that type is processing the way the documentation describes (ETSI 5.14) | 4 |
| Software security is appropriate for the task in regards to cryptography(ETSI 5.3) | 3 |
| Update mechanism cannot be misused(ETSI 5.3) | 4 |
| The update mechanism is effective at verifying the authenticity of an update(ETSI 5.3) | 4 |
| Passwords are stored according to the minimum required security practice. | 5 |
| Hardcoded values are documented as such and are protected by suitable mechanisms, including tamper-resistance. (ETSI 5.4) | 4 |

## Score
We have some crierias for a scoring and evaluating the results of the framework:
1. If a point with 'value of consequence' at '5' and gets value of implementation at '2', the device automaticly gets valued at "Red".
2. Every device with the final score over '' get valued at "RED"
3. Every device that gets a score between '' and '' gets valued at "ORANGE"
4. Every device with a score under '' get valued at "GREEN"


1. for every point:
- consequence * implementation

2. add up every point

- x / 412

3. devide x with 412 (maximum sum) and multiply with 100 to get a 100-point-system.


## Annen scoringsystem

1. for every point:
- Consequence^2 * Implementation^2
2. Add up every point
3. Devide by 100
- x/100
## Interpretation

The lower score, the more secure the device is considered.

- Green: Device is, as far as the test goes, considered safe and utilize personal correctly with proper consent.
- Orange: Device has some weakpoints when it comes to its security or its collection and transmission of data.
- Red: Device has some critical wakpoints that could affect the security of its user; or collection of data is imporperly implemented and data is processed wrongly.

| Green | Orange | Red |
| ----------- | ----------- | ----------- |
| x/100 | x/100 | x/100 |


| Green | Orange | Red |
| ----------| ----------- | -----------|
| x= 0-0.5 | x= 0.5-1 | x= 1++ |
