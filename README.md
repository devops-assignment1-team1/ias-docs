# Introduction
This is the workflow docs for DevOps Oct2022 Team 1. It details the roles of the team members as well as the scrum and development processes that we adhere to.

- [Introduction](#introduction)
  * [Team Members & Roles](#team-members---roles)
  * [Software & Tools](#software---tools)
  * [Tech Stack & Dependencies](#tech-stack---dependencies)
- [Development & Scrum Workflow](#development---scrum-workflow)
  * [Requirements Gathering & Analysis](#requirements-gathering---analysis)
  * [Backlog Issues & Test Cases](#backlog-issues---test-cases)
  * [Development & Git](#development---git)
  * [Pull Requests](#pull-requests)
  * [Completing Issues](#completing-issues)
- [Automation and Communication](#automation-and-communication)
  * [Deployment Strategy](#deployment-strategy)
  * [Delivery Strategy](#delivery-strategy)
  * [Communications Strategy](#communications-strategy)
- [Misc](#misc)
  * [Git Strategy](#git-strategy)
  * [CI/CD](#ci-cd)
  * [Adjusting to Changing Requirements](#adjusting-to-changing-requirements)
  * [Scrum & Processes](#scrum---processes)
- [Pipelines](#pipelines)
## Team Members & Roles
All team members will have to partake in development work
| Name | Role | Description |
|---|---|---|
Dong En | Scrum Master | Facilitate scrum processes and enforces scrum practises
Wen Kang | Lead Developer | Design software architecture and technical requirements
Vernon | Quality Assurance | Test Cases for component and above level tests
Lincoln | Quality Assurance | Test Cases for component and above level tests
Balqis | Developer | Development and more development

## Software & Tools
- **Visual Studio Code**: IDE of choice
- **Github**: Keeps a backup copy of the source files, also serves for remote collaboration for distributed teams.
  - **Github Projects**: Scrum board
  - **Github Actions**: CICD

## Tech Stack & Dependencies
| Name | Description | Link |
|---|---|---|
|Javascript|Backend Language|https://www.javascript.com/|
|ReactJS|Frontend Library|https://reactjs.org/|
|ExpressJS|Backend Framework|https://expressjs.com/|
|Jest|Javascript Testing Framework|https://jestjs.io/|
|MySQL|Relational Database|https://www.mysql.com/|

# Development & Scrum Workflow
Below details the workflow that developers should adhere to during development. It is ordered sequentially.
## Requirements Gathering & Analysis
- Our requriements illication method of choice will be document review
    - After the document review, the scrum master and tech lead will draft out a high level overview of the features required and populate the product backlog with user stories that correspond to the said features
    - The rest of the team will then review and discuss the user stories to polish them
## Backlog Issues & Test Cases
- Creating Issues
  1. Create an issue with a meaningful name in product backlog
  2. Under the issue description
     1. Add in the Requirements section
     2. Add in the Pull Requests section
- Creating Test Cases
    1. Test cases will be created for each user story
        - These tests should be integration or system tests (not unit tests)
        - These test cases should be done in a word document in teams
    2. Test cases should follow the below format
        | ID | Name | Description | Value/Steps | Result |
        |---|---|---|---|---|
        |1|Navigate to contact us|When an existing user .... |1. 2. 3.|url="..."|
## Development & Git
- During Sprint Planning
    1. Assign the issue to a repository
    2. Estimate the issue size
    3. Add a priority
- Starting Development & Branching Issues
    1. Create a branch from the issue and use it for development (e.g. 25-develop locking mechanism)
    2. Assign the issue to yourself and move it to "In Progress"
    3. In the event a new branch is needed, use the same issue number (e.g. 25-new locking mechanism)
    4. Under the description section of each issue, add comments to update the progress of your issue. Developers should only comment important information that is relevant to share to the team. (Subjective, don't put insignificant stuff)
- TDD
    1. Development will be done using a TDD approach (Unit Tests)
    2. Integration and System tests will be introduced after the completion of the relevant features
- Merge Strategy
    1. Development of enhancements or bugs will be done in their respective branches and merged back into main when completed. 
## Pull Requests
- Creating Pull Requests
    1. When code is ready to be merged back into main, developers are to make a pull request
    2. Pull Requests should contain a meaningful description to summarise the changes
    3. Developers are to ping the relevant reviewers in telegram 
    4. If the issue is not linked to the pull request, add the link in the description
- Reviewing Pull Requests
    1. When reviewing pull requests, developers should test the code that has been changed on their own device
    2. To approve the pull request, approve the code or add a LGTM and merge it
## Completing Issues
- Updating Issues & Moving To Review
    1. Ensure that all code is merged into main and working
    2. Ensure that the issue has been updated 
        - Requirements, Pull Requests, Comments/Updates
    3. Move the issue to "In Review" (Max 2 days before Sprint Review)
- Reviewing Issues
    1. Review the requriements of the issue
    2. Verify that the code has been merged into main, deployed and working
    2. Check that the pipeline is passing
    2. Review the code if necessary 
    3. If the issue is done
        1. Add a LGTM
        2. Close the issue
        3. Move it to Ready
    4. If the issue requires changes
        1. Add a comment detailing the change and move it back to "In Progress"

# Automation and Communication
Below details our CI/CD strategy as well as our communications strategy.

## CI Strategy
- CI
    - On push onto development branches
        - Build test, Unit Test 
    - On push/pull request onto main
        - Build test, Unit Test, Integration Test, System Test
        
## Delivery Strategy
- Main will be delivered to relevant stakeholders on a weekly basis
- On acceptance of code, main will be merged into prod

## Deployment Strategy
- Automated deployment will be done for prod on commit/merge
- Deployment will be done in the form of github releases



## Communications Strategy
- Project information will be documented in github projects 
- Documentation will be done in teams files
- Teams will be used for video conferencing
- Telegram will be used for quick texting
- Emails will be used to communicate with relevant stakeholders

# Misc
## Git Strategy
- Merging VS Rebasing
    - The team will be adopting a merging strategy on a feature basis as detailed in the steps above
## Adjusting to Changing Requirements
- If requirements are changed and there is a need to reprioritize the issues, the scrum master and tech lead will review the process of the ongoing sprint and decide to either finish the sprint or introduce new issues.
- The scrum master and tech lead will brief the team on the updated requirements and how/when the team will be taking them on 
## Scrum & Processes
- Working as a team to accomplish sprint goals
    - As a scrum team, the goal of the sprint is to finish the issues in the sprint backlog so members should be helping each other out instead of taking on tasks that are out of scope
    - It is encouraged to seek help from each other when needed not only to improve efficiency but also understanding of the different aspects of the project
- Scrum/Team processes
    - Sprint Planning (Date tbd)
        - Team to discuss resources available, sprint goals, sprint backlog issues 
    - Sprint Review (Date tbd)
        - Team to walkthrough their issue, demo their code and address the Product Owner
        - Code walkthrough can be done after PO leaves
        - Code should be merged into main and deployed in the live environment
    - Sprint Retrospective (Date tbd)
        - Retrotools
        - Actionable points should be documented and worked on in next sprint
    - Technical Backlog Refinement
        - For scrum master and tech lead to discuss the  technical requirements of the project and populate issue requriements
        - Memebers will be asked to join when necessary
    - Architecture Design Sessions
        - For scrum master and tech lead to discuss the architecture and design of the project
        - Memebers will be asked to join when necessary
    - Celebrations
        - It is important to celebrate
        - Hopefully we have time to organise a lunch
- Scrum board
    - Done using Github Projects
# Pipelines
### CI Push WB
- On Push
    - To any Working Branch
- Run build tests
- Run unit tests 
### CI PR Main
- On PR
    -To Main
- Run build tests
- Run unit tests & integration tests
- Create issue if fail
### CI Push Main
- On Push
    - To Main
- Run build tests
- Run unit tests & integration tests
- Generate report
- Upload report 
### CDelivery PR Prod
- On PR
    - To Prod
- Run build tests
- Run unit tests & Integration tests
- Generate report
- Label size of PR
- Zip report and source code
- Notify stakeholder with message and artefacts via telegram
### CDeploy Push Prod
- On Push
    - To Prod
- Run build tests
- Run unit tests & Integration tests
- Generate Report
- Deploy new code
- Notify stakeholder with message and artefacts via telegram
