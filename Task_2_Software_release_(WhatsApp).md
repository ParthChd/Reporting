# Task 2 - Software release (WhatsApp)

##  Test strategy is a set of guidelines that explains test design and determines how testing needs to be done.

### Testing strategy depends on the below key factor :
1. Is the strategy a short term or long term one?
2. Organization type and size.
3. Project requirements – Safety and security related applications require rigorous strategy.
4. Product development model.



### Scope and Overview.

The 12.2v release of whatsapp software will be deployed on production by 16-Sep-2022 as per plan.
QA Team will cover the functional testing of the feature discussed in sprint planning meeting , all the details needs to be added in Requirements specifications documents.
Installation will be tested on the different platforms such as android,iOS and Web.

## Testing Methodology

### Unit testing

_**Purpose**_ : This preliminary test is performed by the development team for testing of individual configuration, custom programs and/or technical services (e.g. Fax, EDI etc.) to ensure that they function according to the detailed technical specification.
Unit test is a white box test and should test all possible flows. Both positive and negative conditions should be tested.
_**Development Phase**_   : Development and Testing.

### Functional Integration Testing

_**Purpose**_ Functional test validates that full operability of interconnected functions, methods or objects within a functional area.  This includes a set of logically related activities or business processes to achieve a defined business process.  
Functional test cases will typically consist of a series business processes or stories joined together to achieve a business process. The smaller size of test cases will enable to test multiple data sets and permutations.
It happens after or in parallel with the development phase as and when all components for a specific flow are complete. Functional test will be done by independent testing team in QA environment.
During subsequent integration testing activities these business process (functional) tests are combined to build end-to-end integration test scenarios.
_**Development Phase**_ Development and Testing.

## User Acceptance Test (UAT)

_**Purpose**_ User acceptance test is performed by business users. The users test the complete, end-to-end business processes to verify that the implemented solution performs the intended functions and satisfies the business requirements.
Development Phase   Final Prep or Implementation.
_**Test Scope**_ UAT and Full Regression.

### Testing Approach

***Regression averse strategy*** with this strategy QA team will get ample time to execute the feature testing and run parrallel automation of the existing feature.
The QA team will mainly emphasize to decrease regression risks for functional or non-functional product shares.


### Testing Environment Specifications

Testing will be taked up on 3 different environment. <br>
Dev Testing on ***Dev server.*** <br>
QA Testing and feature tesing on ***QA server***. <br>
Regression , integration and UAT on ***Preprod server*** <br>


### Testing Tools

TestCase management ***Zephry***. <br>
Front End Automation using ***Espresso*** and ***XCUItest ***. <br>
Backend Automation using ***RestAssured***. <br>
Bug tracking tool ***JIRA***. <br>
***Charles*** for understanding the content in your network call. E.g. Requests sent to the server and data fetched from the server etc. <br>
Performance testing via ***Jmeter***. <br>
Document storage  ***Confluence*** <br>
Backend Manual testing and logs ***Kubernates***. <br>
***Grafana*** for production monitoring. <br>


## Release Control

Feature walk through by Dev team.    ***Dev and Product team*** <br>
Test case review by developer working on the specific feature.  ***QA*** <br>
Feature testing on separate branch.   ***QA*** <br>
Automation Report analysis. ***QA*** <br>
Defect monitoring. ***Leads and Product Team*** <br>

## Defect communication and escalation procedure :

First level of notification to feature related Dev. ***Dev team*** <br>
Daily status review meeting. ***Scrum master*** <br>
Defect disposition meeting. ***Dev and QA*** <br>
Escalation email to development team/SME team manager. ***Mangers*** <br>


### Risk Analysis

UAT need to be performed with first app delivery to QA team. <br>
Backend Deployment need to go +2 days before App release. <br>
UX change to be added on figma. Figma is a browser-based interface design tool <br>
If any new version of OS is releasing need to test on that. <br>


###  Review and Approvals

All these activities are reviewed and sign off by the business team, project management, development team, etc.  <br>

## Proposed Test Cases:

| S.no   | TestCase Description                                                              | Severity         | Priority    |  Comments        | Module       |
| ------ |-----------------------------------------------------------------------------------| -------------- |   -------------|--------------| --------------------------|
| 01     | User is able to download the app from app store and play store.                   | High             | High        | iOS and Android | Installation Testing <br> |
| 02     | User is able to register with a new phone number.                                 | High             | High        | iOS and Android | Installation Testing <br> |
| 03     | User contact are visible to the Whatsapp contact list or not.                     | High             | High        | iOS and Android | Installation Testing <br> | 
| 04     | User phone number should be registered on only one WhatsApp.                      | High             | High        | iOS and Android | Installation Testing <br> |
| 05     | User is able to see unread messages contacts and group-wise.                      | High             | High        | iOS and Android | Usability Testing <br> |
| 06     | User is able to create group and can add others, restricts, removes others        | High             | High        | iOS and Android | UI Testing <br> |
| 07     | User is able to see Scan code screen on mobile phone and login in web.            | High             | High        | iOS and Android | UI + Security Testing <br> |
| 08     | User is able to check active session and log out from all WhatsApp web.           | High             | High        | iOS Android Web | Mainline function <br> |
| 09     | User is able to change number and delete account.                                 | High             | High        | iOS Android Web | Usability Testing <br> |
| 10     | User is able to send and receive message,locations,contact in chatbox and groups. | High             | High        | iOS Android Web | Accessibility Testing  <br> |
| 11     | User is able to make audio and video call to individual contacts and group-wise.  | High             | High        | iOS Android Web | Accessibility Testing <br> |
| 12     | User is able to make payments to individual contacts                              | High             | High        | iOS Android Web | Security Testing  <br> |