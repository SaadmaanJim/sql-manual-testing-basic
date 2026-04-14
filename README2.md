**SQA Manual Testing Basics**

- **My Personal Learning Notes**  
- **Student:** SADMAN  
- **Date:** 11th April, 2026  
- **Goal:** Becoming Expert in Software Quality Assurance (SQA) + Performance Testing
---------------------------------------

# Part-2: Software Testing Life Cycle & Processes

### 1. Software Testing Life Cycle (STLC)
Systematic process with multiple phases performed repeatedly until the product is ready.

### 2. Testing Activities (7 Main Steps)
1. **Test Planning** – Set objectives & strategy  
2. **Test Monitoring & Control** – Track progress  
3. **Test Analysis** – What to test?  
4. **Test Design** – How to test? (create test cases)  
5. **Test Implementation** – Prepare test data & environment  
6. **Test Execution** – Run tests & log results  
7. **Test Completion** – Report, archive, lessons learned

### 3. Testing Roles
- **Test Management Role**: Planning, monitoring, control  
- **Testing Role**: Analysis, design, execution

### 4. Generic Skills of a Good Tester
- Testing knowledge  
- Attention to detail & curiosity  
- Communication & teamwork  
- Analytical & critical thinking  
- Technical knowledge  
- Domain knowledge

### 5. Software Development Life Cycle (SDLC)
Phases: Requirement → Planning → Design → Development → Testing → Deployment

### 6. Types of SDLC Models
- Sequential (Waterfall, V-Model)  
- Iterative (Spiral, Prototyping)  
- Incremental (RAD)

### 7. Agile Methodology

Flexible, iterative, customer-focused approach.

**(A). Core Values of Agile (Agile Manifesto)**
- **Individuals and interactions →** over processes and tools
- **Working software →** over comprehensive documentation
- **Customer collaboration →** over contract negotiation
- **Responding to change →** over following a plan

**(B). 12 Principles of Agile Methodology**
- Customer Satisfaction
- Changing Requirement
- Frequent Delivery
- Promoting Collaboration
- Motivated Individuals
- Face to Face Communication
- Maintain a Constant pace
- Measure Progress
- Technical Excellance
- Simplicity
- Self Organized Teams
- Continuos Improvements

**(C). Popular Agile Frameworks**
-----------------------------------------------------------------------------------------------------------------------------------------------
| Framework                 | Best For                                   | Key Features                                                       |
|---------------------------|--------------------------------------------|--------------------------------------------------------------------|
| Scrum                     | Most common in teams                       | Sprints (2-4 weeks), Daily Standup, Sprint Planning, Retrospective |
| Kanban                    | Support, maintenance, continuous flow      | Visual board (To Do, In Progress, Done), No fixed sprints          |
| SAFe                      | Large enterprises                          | Scaled Agile for big organizations                                 |
| XP (Extreme Programming)  | Early defects, standards, maintainability  |Pair programming, TDD, Continuous Integration                       |
-----------------------------------------------------------------------------------------------------------------------------------------------

**(D). Traditional Testing VS Agile Testing**
---------------------------------------------------------------------------------------------------------------------------------------------
| Aspect                    | Traditional Testing (Waterfall)                          | Agile Testing                                      |
|---------------------------|----------------------------------------------------------|----------------------------------------------------|
| Approach                  | Sequential (Testing is a separate phase)                 | Iterative & Incremental                            |
| When Testing Starts       | After development is fully complete                      | From the very beginning (Shift-Left)               |
| Testing Frequency         | Once, at the end of the project                          | Continuous throughout every sprint                 |
| Requirement Changes       | Very difficult & expensive                               | Welcomes changes even late                         |
| Tester Involvement        | Joins late (after coding)                                | Involved from requirements & planning              |
| Team Structure            | Siloed (Dev vs QA)                                       | Cross-functional (Dev + QA collaborate daily)      |
| Documentation             | Heavy & formal test plans                                | Lightweight & living documents                     |
| Feedback                  | Late feedback                                            | Early & continuous feedback                        |
| Delivery                  | One big release at the end                               | Frequent small releases (every 1-4 weeks)          |
| Automation Focus          | Mostly manual                                            | Strong emphasis on automation                      |
| Defect Detection          | Found very late                                          | Found early & cheap to fix                         |
| Testing Mindset           | "Test after development"                                 | "Quality is everyone's responsibility"             |
| Risk Level                | High                                                     | Low                                                |
---------------------------------------------------------------------------------------------------------------------------------------------

**(E). Role of SQA/Tester in Agile**
- test early and continuously (not only at the end)
- write acceptance criteria with the Product Owner
- do exploratory testing + automation
- attend Daily Standups, Sprint Planning & Retrospectives
- work very closely with developers (Shift-Left Testing)

**(F). Advantages of Agile Testing**
  
   *(i). For the Project*
    - Faster delivery of working software
    - Early bug detection → much cheaper to fix
    - Better adaptability to changing requirements
    - Higher customer satisfaction
    
   *(ii). For the Tester*
    - More involvement and ownership
    - influence the product quality from the start
    - Less repetitive manual regression testing
    - Closer collaboration with developers
    
**(G). Challenges in Agile Testing**
- Requires strong automation skills
- Testers must be technically good (API, UI automation, etc.)
- You need to work at the same pace as developers
- Less time for detailed documentation

**(H). Real-life Example**
  
   **Traditional (Waterfall):**
    - Client provides all requirements at the beginning
    - Development runs for 6 months without testing
    - Testing phase starts only in month 7
    - Many critical bugs and missing features are discovered late
    - Project gets delayed by 2–3 months
    - Final delivery is risky and often doesn't fully meet expectations

  **Agile:**
    - Requirements are broken into small user stories
    - Every 2 weeks (one sprint) new features are delivered
    - Tester starts testing as soon as code is ready (same sprint)
    - Bugs are found early and fixed immediately within the sprint
    - After 3 months, you already have a working, tested, and usable product
    - Customer gives feedback regularly and changes can be incorporated easily

### 8. Activities of Agile (8 Steps)

 Define the project , Create a backlog , Plan the sprint , Execute the sprint , Review and demo , Retrospect , Repeat , Continuously improve

----------------------------------------------------------------------------------------------------------------------------------------------------------------
| Step | Activity                          | Description                                                                 | Key Output                          |
|------|-----------------------------------|-----------------------------------------------------------------------------|-------------------------------------|
| 1    | Understand the Problem / Vision   | Define overall product goal and business needs                              | Product Vision & Initial Backlog    |
| 2    | Create Product Roadmap            | Break vision into major features and prioritize                             | High-level Roadmap                  |
| 3    | Develop/Build the Team            | Form cross-functional team with all required skills                         | Ready self-organizing team          |
| 4    | Sprint Planning                   | Select backlog items and define what to deliver in the sprint               | Sprint Backlog + Sprint Goal        |
| 5    | Daily Scrum                       | 15-min daily sync meeting to discuss progress and blockers                  | Team alignment                      |
| 6    | Sprint Execution                  | Team builds, codes, integrates and tests the features                       | Working tested product increment    |
| 7    | Sprint Review                     | Demo completed work and collect stakeholder feedback                        | Feedback + Updated Backlog          |
| 8    | Sprint Retrospective              | Team reflects on what went well and how to improve next sprint              | Actionable improvements             |
----------------------------------------------------------------------------------------------------------------------------------------------------------------
**Flow:** Step 1-3 (once) → Repeat Step 4-8 every sprint

### 9. Approaches (TDD, BDD, ATDD)

**(i). TDD:**  
- Test-Driven Development
- Write test first → then write code to pass the test → refactor
- Developer
- Unit test code (JUnit, NUnit, pytest)
- Code correctness & design

**(ii). BDD:**
- Behavior-Driven Development
- Describe software behavior from user's perspective using Given-When-Then
- Tester + Product Owner + Dev (Collaboration)
- Given-When-Then (Gherkin language)
- Business behavior & shared understanding

**(iii). ATDD:**
- Acceptance Test-Driven Development
- Write acceptance tests first based on user requirements
- Tester + Product Owner + Dev
- Plain English + Acceptance Criteria
- Business acceptance & requirements

---
