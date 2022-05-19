# Method for evaluation
This is our methodology for scoring the different points, and some more information about the points in the [Framework.md](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md).

## A: Set up user and device   
The main method of evaluating “Set up user” is to go trough the normal setup of the devise and corresponding applications (normally an app on a phone). Everything from setting up your user account to getting the device to function is taken into consideration inn “Set up user”. It is also important to read any documentation like a “user agreement” or similar.  It is important to mention that this “test” dose not care about any difficulty you may have when setting up the device, as this is a security test for the device.

#### A.1: The process is based on consent (GDPR 7)
The first point is a general point for that the whole process from start to finished is consensual, with that we mean that the user have to agree for things to apply to them and the user understands what they are agreeing to. 

## B1: Authentication
Authentication is mostly about the authentications you use to connect to the device/app, often will the username be the users email and therefore the password will be more important than the username. The method you will use to test these points is to first try to change password and figure out the password requirements how long it is, is it required to use special character and numbers. Then you can try to brute force your way into the device/app, it is enough to try the wrong password a handful of times manually. The device/app should have some countermeasure for this. For the third point “Users must be authenticated towards the device to have access to its functionalities and interfaces. (ETSI 5.5)”, it is possible to check it by being logged into two devices and changing the password on one off them, the other device should then be logged off automatically or give you the choise to do so. 

#### B.1.1 and B.1.2: User/data input fields
To check if the input fields for the device/app is protected against attacks, you can try “attacking” the input fields by giving the input SQL, java or other commands, to try to se if it is protected. The commands should not go off at all, and the input field should not be able to recognize that it is a command.  

#### B.1.7: Administrator/user gets notified about new/unauthorized changes in device software (ETSI 5.7) 
This point may be difficult to check, but if you are able to change the device setting without proper authorizations, should an “alarm” go off for the device controler/company and the user should get notified. 

## B2: Security and communication
In this section the most important points are those rergarding cryptographics. What we want to know is what sort of encryption the traffic to and from the device uses. This can be quite hard to find out, but it should be possible. What we demand of the device is that it uses an appropriate encryption algorithm for the task. For example a light bulb does not need the same encryption as a peacemaker. 

## B3: Disclosure of vulnerability
Disclosing of vulnerability  has only two point. In the first you will have to find the vulnerability policy, it may be on the app/application for the device, but normally it will be on its website. A quick google search like “Company_Name vulnerability policy”, will normally do the trick. On the second point about “…act upon vulnerabilities … in a timely manner…”, here we do not expect you to find a vulnerability and then wait for the company to fix it. Instead, you can look for earlier vulnerabilities and se how long they took to fix them.

## C1: Default password
If the device uses a generated password, it is important to check if this password is unique to this device and not used for every device of this kind. It will also have to follow the minimum requirement of having 8 character and having at least one character from each character group (big letters, small letters, and numbers (special characters)). If the device dose not use a default password, then you can give full score for these points.

## C2: Erasure
In this section you will go through the steps to erase your data. This should be an easy process, either a mail to the company or preferable through the app. The process should be written in the Privacy policy, user agreement or other documentations provided with the device/app. 

#### C.2.2: When a user requests erasure of data, third-parties of the company that have the data, will also erase the data.(GDPR 17) (ETSI 5.11)
It will be difficult for a single individual to check this point, the company shall have a description on how they use your data, including if any data is given/sold to third parties. Including how they will erasure the data from the third parties. If this is in order will normally also the erasure process be in order.

#### C.2.5: Nothing indicates that the user data is not erased (ETSI 5.11)
On this point you will only look at you device/app. Look for options you choose last time that the device/app still remembers, and more.

## C3: Personal data
This point mostly about GDPR, and therefore the importance and Value of consequence off these points is higher then average. Points 2, 4, 5, 7, 8, 10 is mostly about the privacy policy. Read the privacy policy and se if they follow the requirement for GDPR and these points.

#### C.3.1: The user is able to edit and complete wrong and uncomplete data without undue delay (GDPR 16)
If the user has any wrong data about themselves, they will then be able to rectify it. Try to change this data, either through app or mail. 

#### C.3.2: All decisions about the user's personal data are based on consent.(GDPR 7)
This point is similar to A.1: The process is based on consent (GDPR 7), with that the point is a general point for that the whole processes that personal data is being used. All decision is understandable for the user, and it is clear what you are consenting to.

#### C.3.3: Users are able to withdraw their consent to use personal data and the processing of personal data at any time. And the process to withdraw is easy to find and understand.(GDPR 7)(ETSI 5.14)
User shall be able to withdraw consent from processes they have previously given consent to. It should be and easy task and preferably through a app or mail.

#### C.3.5: The user is informed about how to express consent (opt-in choice) to the different processes their personal data may be a part of. (ETSI 5.14)
This information shall be in the privacy/user policy, normally you will express consent by agreeing to these policy’s and opt-out by email/deleting your user. Some company’s will make it easier for users to opt-in and out and give the options in the app, often with yes/no sliders for each process.

#### C.3.6: The user shall be provided with all the data the controller/company has of the user within one month from the receipt (GDPR 12)
The user shall be able to request all data the controller/company have off the user, normally through mail. By “from the receipt” will say one month after the company receives your request. You check this by requesting all your data and then looking through it. 

#### C.3.9: Communication with the company is adequate for the request that is made. A confirmation of receival of a request is given.
Good communication with users/customer is a good sign for a company. That the user gets a confirmation that the email has been received by the company and the request is being worked on. After sending a request to the company, see if you get a confirmation, are the confirmation from an employee or is it automatic.   

## D1: Updating and support
The best security recommendations are normally to update your devices/programs. The company can protect the devices by supporting it and updating it, this period should at least be 5 years. The device should be able to update it itself automatically, and it is recommended to give the user information that an update is taking place and to give the user the ability to check for updates. This information should be in one of the policies or on the app. 

#### D.1.6: Everything enabled by default is necessary for the device (ETSI 5.6)
There will normally be many default decision/values already in the app/device, you can go through the app and see if any of default values is not necessary for the use of the device. You should also check for open ports and their functionalities, this can you do by using some of the tools in “tools.md”.

## D2: Physical
This section is about the device physical aspects. 

#### D.2.1: Device is made by adequate physical material for its use case (Enisa)
Here will “adequate physical material” mean that the material will not be easily broken into, either by mistake or with intent. If the device is to be used outdoors/public the requirement will rise. 

#### D.2.2: All exposed interfaces (Physical) are covered, protected or enabled as required, and accessible physical debug interfaces are disabled(ETSI 5.6)
Any open USB or other “entrances” to the device it closed/covered if it is not used by the user.

## E: Further tests that require specialized knowledge
The E-table in the frameowrk have all the point that require specialized knowledge. We will not give any methods for these points, but we include them because of the relevancy.
