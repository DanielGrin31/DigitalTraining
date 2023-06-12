# DevOps Summary

## Table Of Contents
- [What Is DevOps?](#what-is-devops)
- [Test Driven Development](#test-driven-development)
-  [Version Control](#version-control)
- [Infrastructure As Code](#)
- [CI/CD](#cicd)
- [Agile Development](#agile-development) 
- [Microservices](#microservices)


## What Is DevOps?
DevOps Is a methodology that helps engineering teams build products by continuously getting user feedback.

![](./assets/images/devops.png)

This approach allows you to continuously upgrade software instead of creating a new version of it every time.  
The steps of DevOps are:

1.  **Plan:** This stage involves understanding the product requirements, defining the architectural design, and planning how the application will be developed.
    
2.  **Code:** In this stage, developers write the code to implement the planned features and functionality of the application.
    
3.  **Build:** The code is built by compiling or transforming it into an executable format. This typically involves tasks such as compiling, packaging, and generating artifacts.
    
4.  **Test:** The application is tested to ensure its functionality, quality, and performance. This includes automated tests as part of continuous integration and manual testing by quality assurance teams.
    
5.  **Release:** Once the application passes the testing phase, it is prepared for deployment. This stage involves using continuous deployment strategies to deploy the new version of the application without disrupting the entire user base.
    
6.  **Deploy:** The new version of the application is deployed to the production environment, making it accessible to users.
    
7.  **Operate:** In this stage, the application is actively monitored, scaled, and managed in the production environment. This includes allocating resources, configuring the environment, and ensuring the application's availability and performance.
    
8.  **Monitoring:** Ongoing monitoring and feedback collection help gain insights into the application's performance, usage patterns, and user interactions. This information is valuable for making informed decisions and identifying areas for improvement.
    
9.  **Repeat:** The DevOps process is iterative and continuous. After deployment and operation, the cycle starts again with further planning, development, testing, and refinement.


## Test Driven Development
TDD is a coding methodology where tests are written before code is written.  
In TDD, the development process follows a cycle of writing a test, implementing the code to make the test pass, and then refactoring the code.  
The process of TDD is as follows:

1. **Create Test:** A developerwrites a test case that defines the desired behavior of the code.

2. **Run Test:** The developer runs the test, which should fail since the code is not implemented yet.

3. **Write Code:** The developer writes the minimum amount of code necessary to make the test pass.

4. **Run Test Again:** After implementing the code, the developer runs the test again to verify that it passes.

5. **Refactor Code:** Once the test passes, the developer refactors the code to improve its design, readability, and maintainability while keeping all the tests passing.

6. **Repeat:** The process is repeated for the next set of desired functionality or changes. Each cycle involves writing a test, implementing the code, running the test, and refactoring.


By following TDD, developers can ensure that their code is tested thoroughly and that it meets the desired requirements. 
### Test Types

**Unit Tests:** these ensure that all components work on their own  
**Integration Tests:** these ensure multiple components work together  
**End-To-End Tests:** these ensure the whole system works together (E2E,System Tests)  
**Acceptance Tests:** these ensure the satisfaction of clients with the system  

## Version Control

### Pull Request Automation
this refers to the automation of processes and tasks associated with managing pull requests in software development workflows.  
It involves using technologies to automate and optimize the steps involved in creating, reviewing, and merging pull requests.  

>Basically this means letting the developers know as soon as possible wether or not their change to the code is good or bad

The pull request is reviewed by at least one programmer in a code review where the programmer will check if the new changes comply with the code style,wether or not there are architectural problems etc. .
>These cannot be automated

After the coding review is done a product manager in charge of the functionality being proposed will give feedback.

The goal of this process is for a developer to be able to propose a change and get that change merged into the source code in the shortest time possible while maintaining correct code.

### Git

## Infrastructure As Code

### Terraform

## CI/CD
### Deployment Automation
Deployment automation has multiple goals,in addition to optimizing deployment efficiency it also: Deploys a feature to a set of users before releasing it publicly, starting new versions of services without causing downtime and rolling back services to previous versions in case an issue occurs.

### Continuous Integration
CI or Continuous integration refers to the ability of developers to continuously push small updates to a central repository frequently,then those changes are verified by an automatic software that runs tests to ensure no major issues are seen by the customers 

By practicing CI, development teams can catch integration issues early, identify bugs or conflicts, and ensure that the codebase remains in a functional and stable state.  
CI helps to minimize the risks associated with merging code changes from multiple developers and promotes collaboration, as developers regularly integrate their work, enabling faster feedback and reducing the time between code changes and their validation.

To Achieve CI developers often make use of a branch-based development process.  

First developers "copy" the current source code that is presented to the customers at that point in time into a new branch called the **Feature Branch**, they then make changes to the source code and work independently from other teams on the various components.  

Then,still on the feature branch theyll "push" the updates onto the repistory still not interacting with the main code,that repository will run the configured CI tests.  

Finally the developer working on the feature branch makes a pull request asking to merge their code into the main code repository with the CI tests attached.
#### Code Coverage
It is a metric that measures how much of the code is "covered" by the tests of the CI/CD process,it is used to assess how thorough the tests are and helps developers identify areas of the code that are not adequately tested.  
It helps prevent untested or poorly tested code from being promoted to production, reducing the risk of bugs and issues in the live environment.

Code Coverage is measures by the number of non-sntax lines executed by tests divided by the total number of non-syntax lines  
$$Code Coverage= \frac{ExecutedNonSyntaxLines}{AllNonSyntaxLines}$$

**Branch coverage** measures the coverage of groups of lines by tests instead of all lines,meaning how many groups of code are measures,groups can be a body of an if statement or a function etc.
### Jenkins

## Agile Development

## Microservices
## Monitoring
### Application Performance Management
It ensures that metrics such as request processing time,number of servers used and other key health metrics are processed and if theres a problem the appropriate people responsible for the operation of the service are notified and can respond to it.  

It also includes logging of all events relating to a service allowing us to infer conclusions from them and improve upon them.  

If the metrics indicate theres an issue with the load amount on the servers it allows for them to automatically scale based on those metrics.



<scripts>
<html><head>
	
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>
<script type="text/javascript"
        src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
</head></html>
</scripts>