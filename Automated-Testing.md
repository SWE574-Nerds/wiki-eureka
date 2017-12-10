### What Types of Software Testing To Perform
1. Data-driven Testing :  Executing same scenario multiple times for different data sets.  
2. Behaviour-Driven Development: Collaboration between Business stakeholders, Business Analysts, QA Team and developers. Tests should be automated using in plain meaningful English text using a simple grammar defined by a language called Gherkin.  

### What Test Cases to Automate
1. Repetitive tests that run for multiple builds
1. Tests that require multiple data sets.

### Tools to Use: 
1. Cucumber
1. Selenium
1. Java
1. JUnit
1. Chrome Driver

### Sample Test Cases 

All tets cases should be defined in feature files.

**Scenario Outline:** Scenario description  
    **Given** Given condition for test  
    **When** Action step for test with given "param"          
    **Then** Expected result for test               
 
     Examples:  
       | param         |
       | patameter1    |
       | paramater2    |

### Automated Test Project

[Test project path](https://github.com/SWE574-Nerds/friendly-eureka/tree/master/tests/friendlyeureka)

### Running Automated Tests
To run automated test please run the commands below:  

> cd /friendly-eureka/tests/friendlyeureka  
> mvn test