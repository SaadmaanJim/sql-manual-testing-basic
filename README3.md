**SQA Manual Testing Basics**

- **My Personal Learning Notes**  
- **Student:** SADMAN  
- **Date:** April 12th , 2026  
- **Goal:** Becoming Expert in Software Quality Assurance (SQA) + Performance Testing

-----------------

# Part-3: Testing Types, Levels & Techniques

## 1. Software Testing Classification

 ### (i). Based on Action
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

## (ii). Based on Approach
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

## (iii). Based on Techniques
         
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


## 2. Static Testing vs Dynamic Testing
------------------------------------------------------------------------------------------------------------------
| Aspect                    | Static Testing                          | Dynamic Testing                          |
|---------------------------|-----------------------------------------|------------------------------------------|
| Code Execution            | No execution required                   | Requires code execution                  |
| Defect Detection          | Finds defects directly                  | Causes failures → then finds defects     |
| Work Products             | Documents, code, designs                | Running software                         |
| Best For                  | Early defects, standards, maintainability | Functional & non-functional behavior   |
------------------------------------------------------------------------------------------------------------------

## 3. Functional vs Non-Functional Testing         

**(i). Functional Testing**
 
  Functional Testing is a type of black-box testing that verifies whether the software system works as per the functional requirements specified in the             requirement document.

**(ii.) Non-Functional Testing**
  
  Non-Functional Testing is a type of testing that verifies how well the system performs, rather than what the system does.


## (i). Funcional Testing

*(i). Feature Testing*

- **Defination:** Testing individual features/functions to ensure they work as per requirements.
- **Real-Life Example:** Testing the “Add to Cart” button in an e-commerce app — check if item is added correctly, quantity updates, price calculates properly.
- **When it is done?** During System Testing

*(ii). Smoke Testing*

- **Defination:** Basic “is the build even testable?” test. Quick check of major functionalities to see if the build is stable enough for further testing.
- **Real-life Example:** After a new build is deployed, tester quickly checks: Can I login? Can I see the homepage? Can I navigate to main menu? If these fail →                           build is rejected.
- **When it is done?** Right after every new build

*(iii). Sanity Testing*

- **Defination:** TestingFocused & narrow testing to verify that a specific change/fix didn’t break related areas. It’s like a quick health check after a fix.
- **Real-Life Example:** TestingFocused & narrow testing to verify that a specific change/fix didn’t break related areas. It’s like a quick health check after a                           fix.
- **When it is done?** After bug fix or small change

*(iv). Regression Testing*

- **Defination:** Re-testing the previously tested features to make sure that new changes or bug fixes have not introduced new bugs in existing functionality.
- **Real-life Example:** After adding “Payment Gateway”, tester re-checks Login, Add to Cart, Order History, Profile — to ensure nothing broke.
- **When it is done?** After every code change / sprint

*(iv). Exploratory Testing*

- **Defination:** Testing without formal test cases. Tester explores the application like a real user, using creativity, intuition, and domain knowledge to find                    bugs.
- **Real-life Example:** Tester opens a new food delivery app and tries different flows: ordering while offline, changing address during checkout, applying                                coupon + cashback together, etc.
- **When it is done?** Any time, especially early stages

*(v). Ad-hoc Testing*

- **Defination:** Informal, unstructured testing done without any documentation or test cases. Random testing based on tester’s mood and experience.
- **Real-Life Example:** Tester suddenly thinks “What if I click this button 50 times quickly?” and tries it. No plan, just random clicking.         
- **When it is done?** Anytime, usually by experienced testers

*(vi). Monkey Testing*

- **Defination:** Random input testing (like a monkey randomly pressing buttons). Can be dumb monkey (completely random) or smart monkey (some logic).
- **Real-Life Example:** In a mobile app, tester or tool randomly taps anywhere on screen, enters garbage text, rotates screen suddenly, etc.        
- **When it is done?** To find unexpected crashes

  *(vii). Gorilla Testing*

- **Defination:** Heavy, repetitive testing on one single module/feature to check its robustness.
- **Real-Life Example:** Testing the “Login” screen 1000 times with different usernames, passwords, special characters, copy-paste, etc.         
- **When it is done?** For critical modules

  *(viii). Alpha Testing*

- **Defination:** Testing done by the internal team (developers + testers) in the development environment before releasing to real users.
- **Real-Life Example:** Before launching the app, the company’s own employees use the app and report bugs.           
- **When it is done?** Before Beta release


  *(ix).Beta Testing*

- **Defination:** Testing done by real users in their real environment before final release. Feedback is collected from actual customers. 
- **Real-Life Example:** Company releases the app to 500 selected users. Users use it in their daily life and report issues (network problems, battery drain,                              etc.).           
- **When it is done?** Just before public launch

*(iii). A/B Testing*

- **Defination:** Comparing two versions (A and B) of the same feature to see which one performs better (based on user behavior).
- **Real-Life Example:** Showing two different “Buy Now” button colors (red vs green) to different users and checking which one gets more clicks and sales.      - **When it is done?** In live production (after launch)

## (ii). Non-functional Testing

*(i). Perfomance Testing*

- **Defination:** Testing how fast, stable, and responsive the system is under different loads and conditions.
- **Real-Life Example:** Checking how long an e-commerce website takes to load the product page when 5,000 users are shopping at the same time.         
- **When it is done?** Users hate slow apps. Poor performance = lost customers and revenue.

*(ii). Security Testing*

- **Defination:** Testing whether the system is protected from unauthorized access, attacks, and data leaks.
- **Real-Life Example:** Trying SQL Injection, XSS attacks, checking if login is secure, testing password encryption, session hijacking, etc.      
- **When it is done?** Protects sensitive user data (bank details, personal info). One breach can destroy a company’s reputation.

*(iii). Usability Testing*

- **Defination:** Testing how easy, intuitive, and user-friendly the application is for end users.
- **Real-Life Example:** Giving the app to 10 real users and observing: Can they complete registration easily? Is the navigation confusing? Do they get stuck?    
- **When it Matters?** Even if the app works correctly, if users find it difficult to use, they will leave.

*(iv). Cross Browser / Device Testing Testing*

- **Defination:** Testing whether the application works correctly on different browsers, devices, screen sizes, and operating systems.
- **Real-Life Example:** Checking the website on Chrome, Firefox, Safari, Edge + on Android phone, iPhone, Tablet, Desktop with different resolutions.        
- **When it Matters?** Users access your app from many devices. It must look and work properly everywhere.

*(v). Benchmark Testing*

- **Defination:** Comparing the performance of your system against a standard, competitor, or previous version to measure improvement.
- **Real-Life Example:** Comparing your app’s login time (2.5 sec) with a competitor’s app (1.8 sec) or with the previous version of your own app.          
- **When it Matters?** Helps set performance goals and prove that your system is getting better over time.





























































