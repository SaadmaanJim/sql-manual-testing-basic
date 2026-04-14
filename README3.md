**SQA Manual Testing Basics**

- **My Personal Learning Notes**  
- **Student:** SADMAN  
- **Date:** April 12th/13th/14th , 2026  
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

*(xi). A/B Testing*

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

## 4. Good Testing Practices
- Every development activity should have a corresponding test activity
- Different test levels have specific objectives
- Start testing early (Shift-Left approach)
- Testers should review documents as soon as drafts are ready

Good Testing Practices are the habits that professional SQA teams follow to deliver better quality software faster and with fewer bugs.

#### (A). Every development activity should have a corresponding test activity
**Meaning**: Whatever developers build, testers should test it. Testing should happen in parallel with development.

**Real-world Example**:  
In a **Food Delivery App** (like Pathao Food):
- When developers build "Order Placement" feature → Testers immediately create test cases for it.
- When developers integrate "Payment Gateway" → Testers plan functional, security, and performance testing.

#### (B). Different test levels have specific objectives
**Meaning**: Each testing level (Unit, Integration, System, Acceptance) has its own goal.

**Real-world Example** (Food Delivery App):
- **Unit Testing**: Check if "Calculate Delivery Charge" function works correctly.
- **Integration Testing**: Check if Login + Cart + Payment work together smoothly.
- **System Testing**: Test the complete flow from selecting food to receiving order.
- **Acceptance Testing**: Customer checks if the app meets their business needs.

#### (C). Start testing early (Shift-Left Approach)
**Meaning**: Testing should begin as early as possible in the project, not just at the end.

**Real-world Example**:
- **Bad Way**: Development finishes completely, then testing starts → Many critical bugs found → Project gets delayed.
- **Good Way (Shift-Left)**: Testers review requirements in Week 1, design in Week 2, and start writing test cases while developers are still coding → Bugs are caught early → Less rework → Project delivered on time.

**Benefit**: Fixing a bug in the requirement phase is 100 times cheaper than fixing it after launch.

#### (D). Testers should review documents as soon as drafts are ready
**Meaning**: Testers must review requirements, designs, and user stories immediately when drafts are shared.

**Real-world Example**:
Business Analyst shares a draft requirement for "Promo Code System".  
Tester reviews it the same day and asks:
- What happens if a user applies two promo codes together?
- What is the maximum discount limit?
- Can expired promo codes be used?

→ Requirements become clearer before development starts → Fewer defects later.

**Summary**:  
Good Testing Practices mean **testing early, testing continuously, and testing smartly** alongside development.

## 5. Independence of Testing
- No Independence → Author tests own work
- Some Independence → Peers in same team
- High Independence → Testers from other teams
- Very High Independence → External testers

Independence of Testing means **how much distance** there is between the person who developed the code and the person who is testing it.  
The more independent the tester is, the more objective and effective the testing becomes.

#### Levels of Independence
----------------------------------------------------------------------------------------------------------------------------------------------------------------
| Level                    | Who Tests the Work?                          | Objectivity | Real-World Scenario                                                  |
|--------------------------|----------------------------------------------|-----------|---------------------                                                   |
| **No Independence**      | Author (Developer tests his own code)        | Very Low  | Developer writes "Fund Transfer" feature and tests it himself. He may  |  |                                                                                          miss obvious bugs because he is biased.                             |
| **Some Independence**    | Peers from the same team                     | Low       | Another developer in the same team reviews and tests the code.         |
| **High Independence**    | Testers from other teams inside the company  | High      | A dedicated tester from the "Payments Testing Team" (different team)   |  |                                                                                       tests the feature thoroughly.                                          |
| **Very High Independence**| External testers / Third-party company      | Very High | The bank hires an external QA & Security company to perform penetration|  |                                                                                        testing.                                                              |
----------------------------------------------------------------------------------------------------------------------------------------------------------------
#### Real-Life Scenario: Mobile Banking App (bKash / Nagad)

**Project**: Adding a new "Fund Transfer" feature.

- **No Independence**: The developer who coded the feature tests it himself. He only tests the "happy path" and misses a critical bug — user can transfer money even with zero balance.
- **Some Independence**: A teammate tests it. He finds some issues but may hesitate to report harshly due to team relationship.
- **High Independence**: A tester from the separate "Core Banking Testing Team" tests the feature. He finds the zero-balance bug, security loopholes, and improper error handling.
- **Very High Independence**: The bank hires an external cybersecurity firm. They discover not only the zero-balance issue but also API vulnerabilities, session hijacking risks, and data leakage possibilities.

**Result**: Higher independence → More critical bugs found → Safer and more reliable app.

#### Additional Real-Life Examples from Different Domains

1. **E-commerce App (like Daraz)**:
   - High Independence: A tester from the "Checkout Team" tests the "Product Recommendation Engine" built by the AI Team.
   - Very High Independence: External QA company tests the payment gateway before Eid sale.

2. **Education App (like 10 Minute School or AIUB Portal)**:
   - High Independence: Testers from the "Exam Module Team" test the "Result Publishing" feature developed by another team.
   - Very High Independence: External auditors test the entire exam result system before publishing board exam results.

#### Why Independence Matters
- Reduces bias and "blind spots"
- Increases the chance of finding hidden and critical bugs
- Improves overall software quality and security
- Especially important for banking, payment, healthcare, and government systems

**Best Practice**: In most professional Agile teams, we aim for **High Independence**. For critical features, we go for **Very High Independence**.

## 6. Test Levels (example with food-delivery APP)

### (a). Component / Unit Testing

- **Defination:** Testing individual small units or components of the code in isolation.
- **Objectives:** Check individual functions work correctly
- **Who Does It?** Developers
- **Real-world Example:** Testing the "Calculate Delivery Fee" function to check if VAT and delivery charge are calculated correctly.

### (b). Integration Testing (Component Integration + System Integration)

- **Defination:** Testing the interaction and data flow between different modules/components when combined. (Includes Component Integration and System                              Integration)
- **Objectives:** Check if different modules work together
- **Who Does It?** Developers + Testers
- **Real-world Example:** Checking if Login module works correctly with Cart module and Payment module when placing an order.

### (c). System Testing

- **Defination:** Testing the complete integrated software system as a whole against the requirements.
- **Objectives:** Check the complete app as a whole
- **Who Does It?** Dedicated Testers
- **Real-world Example:** Testing the full end-to-end flow: Browse restaurants → Select food → Add to cart → Payment → Order tracking.

### (d). Acceptance Testing

- **Defination:** Testing to verify whether the system meets the business and user requirements and is ready for release.
- **Objectives:** Check if the app meets business/user needs
- **Who Does It?** Client / End Users / Stakeholders
- **Real-world Example:** Restaurant owners and real customers test the app to confirm it is usable and meets their expectations before final launch.

## 7. Test Pyramid
- **Bottom →** Many small, fast tests (Unit tests)
 *Real-life Example* ->
  - Test if delivery charge is calculated correctly (including VAT)
  - Test if promo code discount is applied properly
  - Test if minimum order value validation works
→ You may write hundreds of these tests.

- **Middle →** Service / Integration tests
 *Real-life Example*
  - Test if Login API returns correct user data
  - Test if Cart API + Payment API work together
  - Test if Order API updates restaurant inventory correctly
     → You may write 50–100 of these tests.

- **Top →** Few slow, broad tests (UI / End-to-End tests)
  *Real-life Example*
  - Test the complete user journey:
  - Open app →
  - Login →
  - Browse restaurants →
  - Add food →
  - Checkout →
  - Make payment →
  - See order status
→ You should write only 10–20 of these tests.

## 8. Test Quadrants

### Q1: Technology Facing + Support the Team (Unit, Component, CI)
 
  - **Type:** Technology Facing + Support the Team
  - **Purpose:**
  - **Who usually does it:**
  - **Real-life Example:** 

### Q2: Business Facing + Support the Team (Functional, User Story, API)
 
  - **Type:**
  - **Purpose:**
  - **Who usually does it:**
  - **Real-life Example:** 

### Q3: Business Facing + Critique the Product (Exploratory, Usability, UAT)
  
  - **Type:**
  - **Purpose:**
  - **Who usually does it:**
  - **Real-life Example:** 



### Q4: Technology Facing + Critique the Product (Performance, Security, Load, Regression)
  
  - **Type:**
  - **Purpose:**
  - **Who usually does it:**
  - **Real-life Example:** 














































