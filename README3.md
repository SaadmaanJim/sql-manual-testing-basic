**SQA Manual Testing Basics**

- **My Personal Learning Notes**  
- **Student:** SADMAN  
- **Date:** April 12th , 2026  
- **Goal:** Becoming Expert in Software Quality Assurance (SQA) + Performance Testing

-----------------

## Part-3: Testing Types, Levels & Techniques

### 1. Software Testing Classification

 **(i). Based on Action:**
---------------------------------------------------------------------------------------------------------------------------------------------------------
| Aspect                    | Manual Testing                                              | Automation Testing                                          |
|---------------------------|-------------------------------------------------------------|-------------------------------------------------------------|
| Definition                | Testing software manually by a human tester                 | Using tools/scripts to run tests automatically              |
| Execution                 | Tester performs tests by hand (clicking, typing, observing) | Scripts run tests without human intervention                |
| Speed                     | Slow                                                        | Very Fast                                                   |
| Cost                      | High in long run (needs repeated human effort)              | High initial cost, low in long run                          |
| Accuracy                  | Prone to human error                                        | Highly consistent and accurate                              |
| Best For                  | Exploratory testing, Usability, Ad-hoc, UI/UX testing       | Regression testing, Smoke, Sanity, Performance, API testing |
| Reusability               | Low (same test repeated manually every time)                | High (scripts can be reused forever)                        |
| Test Coverage             | Limited due to time constraint                              | High (can run thousands of tests quickly)                   |
| Initial Setup             | No setup required                                           | Requires framework, tools, and scripting effort             |
| Maintenance               | Easy to change                                              | High maintenance when application changes                   |
| Skills Required           | Domain knowledge, analytical thinking                       | Programming + Testing knowledge                             |
| When to Use               | Early stages, new features, one-time testing                | Stable features, repetitive tests, large projects           |
---------------------------------------------------------------------------------------------------------------------------------------------------------

**(ii). Based on Approach**
--------------------------------------------------------------------------------------------------------------------------------------------------------
| Aspect                  | Static Testing                                              | Dynamic Testing                                              |
|-------------------------|-------------------------------------------------------------|--------------------------------------------------------------|
| Definition              | Testing without executing the code                          | Testing by executing/running the code                        |
| Execution               | No code execution required                                  | Code must be executed                                        |
| When it is performed    | Early stage (before coding or compilation)                  | After code is compiled and running                           |
| Objective               | Find defects in documents, requirements, and code           | Validate actual behavior and functionality                   |
| Cost                    | Very low (cheaper to fix early)                             | Higher (defects found later)                                 |
| Techniques              | Reviews, Walkthroughs, Inspections, Static Code Analysis    | Functional & Non-functional testing                          |
| Tools                   | SonarQube, ESLint, PMD, Checkstyle, Review tools            | Selenium, JUnit, Postman, JMeter, Appium                     |
| Best For                | Requirements, Design docs, Source code, Test cases          | Runtime behavior, UI, API, Performance                       |
| Defect Detection        | Very early (prevention)                                     | Later stage (detection)                                      |
| Human Involvement       | High (manual reviews)                                       | Medium to High                                               |
| Reusability             | Low                                                         | High (especially with automation)                            |
--------------------------------------------------------------------------------------------------------------------------------------------------------

**(iii). Based on Techniques**
  *(a). Black Box*
-----------------------------------------------------------------------------------------------------------
| Aspect                    | Description                                                                 |    
|---------------------------|-----------------------------------------------------------------------------|
| Definition                | Testing the software without knowing its internal code structure            |
| Tester's View             | End-user / external perspective                                             |
| Knowledge Required        | Only requirements, specifications, and expected outputs                     |
| Focus                     | What the system does (inputs vs outputs)                                    |
| Techniques                | Equivalence Partitioning, Boundary Value Analysis, Decision Table, Use Case |
| Best For                  | Functional testing, System testing, Acceptance testing                      |
| Execution                 | Can be manual or automated                                                  |
| Tools                     | Selenium, Postman, JMeter, Manual testing tools                             |
| Advantage                 | Unbiased, user-focused, no need for coding knowledge                        |
| Limitation                | Limited code path coverage                                                  |
-----------------------------------------------------------------------------------------------------------
       
*(b). White Box*
-----------------------------------------------------------------------------------------------------------
| Aspect                    | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| Definition                | Testing with full knowledge of internal code structure and logic            |
| Tester's View             | Developer / technical perspective                                           |
| Knowledge Required        | Programming skills, code, architecture, and logic flows                     |
| Focus                     | How the system works (code coverage)                                        |
| Techniques                | Statement Coverage, Branch Coverage, Path Coverage, Condition Coverage      |
| Best For                  | Unit testing, Integration testing                                           |
| Execution                 | Mostly automated                                                            |
| Tools                     | JUnit, NUnit, JaCoCo, SonarQube, Code coverage tools                        |
| Advantage                 | Thorough structural coverage, finds hidden logic errors                     |
| Limitation                | Time-consuming, requires strong programming skills                          |
-----------------------------------------------------------------------------------------------------------

*(c).Experienced-Based*
-----------------------------------------------------------------------------------------------------------
| Aspect                    | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| Definition                | Testing based on the tester's skill, intuition, and past experience         |
| Tester's View             | Experienced tester perspective                                              |
| Knowledge Required        | Domain knowledge + common bug patterns + intuition                          |
| Focus                     | What might go wrong based on real-world experience                          |
| Techniques                | Exploratory Testing, Error Guessing, Checklist-based, Attack Testing        |
| Best For                  | Finding hidden/edge-case bugs, usability issues, regression                 |
| Execution                 | Mostly manual (Exploratory)                                                 |
| Tools                     | No specific tools — relies on tester's mind and experience                  |
| Advantage                 | Finds bugs that formal tests often miss                                     |
| Limitation                | Highly depends on the individual tester's skill and experience              |
-----------------------------------------------------------------------------------------------------------

