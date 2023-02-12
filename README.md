# Introduction
This is the workflow docs for DevOps Oct2022 Team 1. It details the roles of the team members as well as the scrum and development processes that we adhere to.

- [Introduction](#introduction)
  * [Project Documentation](#project-documentation)
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
  * [CICD Strategy](#cicd-strategy)
  * [Monitoring Strategy](#monitoring-strategy)
  * [Test Metrics](#test-metrics)
  * [Communications Strategy](#communications-strategy)
- [Misc](#misc)
  * [Git Strategy](#git-strategy)
  * [Adjusting to Changing Requirements](#adjusting-to-changing-requirements)
  * [Scrum & Processes (IGNORE)](#scrum---processes--ignore-)

## Project Documentation
Files/Links for technical documentation
| Name |  Link |
|---|---|
Technical Requirement Specifications | google doc
Solution Architecture | lucidchart 
Wireframe | Figma
Integration Test Cases | MS Word

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
|ExpressJS|Backend Framework|https://expressjs.com/|
|Jest|Javascript Testing Framework|https://jestjs.io/|
|MySQL|Relational Database|https://www.mysql.com/|
|Selenium|Web Application Automator|https://www.selenium.dev/|

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
    1. Test cases will be created for each user story that is worked on during that sprint
        - These tests should be integration or system tests (not unit tests)
        - These test cases should be done in a word document in teams
    2. Test cases should follow the following format
        | ID (User Story • No.)| Module | Scenario | Description | Value/Steps | Result |
        |---|---|---|---|---|---|
        |As a user I want to ... so that ... • T-1 |Modules involved in test case|Action performed by user for an output|This test case is to verify/ensure that ...|1. 2. 3.|The website should ...
    3. A manual test will be conducted before sprint review and if there are no issues it will be converted to integration tests in the subsequent sprint
## Development & Git
- During Sprint Planning
    1. Assign the issue to a repository
    2. Estimate the issue size
- Starting Development & Branching Issues
    1. Read and fill out the requirements for the issue
    2. Create a branch from the issue and use it for development (e.g. 25-develop locking mechanism)
    3. Assign the issue to yourself and move it to "In Progress"
    4. In the event a new branch is needed, use the same issue number (e.g. 25-new locking mechanism)
    5. Under the description section of each issue, add comments to update the progress of your issue. Developers should only comment important information that is relevant to share to the team. (Subjective, don't put insignificant stuff)
- TDD
    1. Development will be done using a Ping Pong Programming approach
    2. Integration and System tests will be introduced after every sprint
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
    3. Move the issue to "In Review" (Max 1 days before Sprint Review)
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

## CICD Strategy && Monitoring Strategy
 
## Test Metrics
- Unit Tests & Intgeration Tests
    - 100% Pass
- SonarCloud Quality Gate (to pass)
  - Test Coverage > 80.0%
  - Duplicate Lines < 3.0%
  - Maintainabbility Rating (Code Smell) > A
  - Reliability Rating (Bugs) > A
  - Securty Hotspots Reviewed > 100.0%
  - Secruity Rating (Vulnerabilities) > A

## Communications Strategy
- Project information will be documented in github projects and relevant repos
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
    - Sprint Planning (Thursday)
        - Team to discuss resources available, sprint goals, sprint backlog issues 
        - Scrum board to be documented
    - Sprint Review (Wednesday)
        - Team to walkthrough their issue, demo their code and address the Product Owner
        - Code walkthrough can be done after PO leaves
        - Code should be merged into main and deployed in the live environment 
        - Scrum board to be documented
    - Sprint Retrospective (Wednesday)
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
