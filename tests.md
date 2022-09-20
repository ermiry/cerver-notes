# Tests

**From IBM**
Software testing is the process of evaluating and verifying that a software product or application does what it is supposed to do. The benefits of testing include preventing bugs, reducing development costs and improving performance.

## Importance
Software Testing is Important because if there are any bugs or errors in the software, it can be identified early and can be solved before delivery of the software product. Properly tested software product ensures reliability, security and high performance which further results in time saving, cost effectiveness and customer satisfaction.

## Types
**From IBM**
- **Acceptance testing:** Verifying whether the whole system works as intended.
- **Unit testing:** Validating that each software unit performs as expected. A unit is the smallest testable component of an application.
- **Integration testing:** Ensuring that software components or functions operate together.
- **Performance testing:** Testing how the software performs under different workloads. Load testing, for example, is used to evaluate performance under real-life load conditions.
- **Regression testing:** Checking whether new features break or degrade functionality.
- **Stress testing:** Testing how much strain the system can take before it fails.

## Continuous Testing
**From IBM**
Project teams test each build as it becomes available. This type of software testing relies on test automation that is integrated with the deployment process. It enables software to be validated in realistic test environments earlier in the process which improves design and reduces risks.

## Code Coverage
**Erick Salas**
Code coverage is a metric that can help assess the quality of the defined tests as it indicates how much of the source code is executed when a test suite is run. A program with a higher test coverage score has a lower chance of containing undetected software bugs in a production environment.

**From Atlassian**
Code coverage tools will use one or more criteria to determine how the code was exercised or not during the execution of your test suite. 

- **Function coverage:** How many of the functions defined have been called.
- **Statement coverage:** How many of the statements in the program have been executed.
- **Branches coverage:** How many of the branches of the control structures (if statements for instance) have been executed.
- **Condition coverage:** How many of the boolean sub-expressions have been tested for a true and a false value.
- **Line coverage:** How many of lines of source code have been tested.

These metrics are usually represented as the number of items actually tested, the items found in your code, and a coverage percentage (items tested / items found).

## Tools
### Codecov
**From Codecov**
Codecov highlights which portions of your code that have not been properly tested or may require additional testing, then generates a report on your test suite’s code coverage, and overlays that directly onto your source code, making it even easier to identify needed test areas.

### GitHub Actions
**From GitHub**
GitHub Actions is a continuous integration and continuous delivery (CI/CD) platform that allows you to automate your build, test, and deployment pipeline. Workflows can be created to build and test every pull request on a repository, or to deploy merged pull requests to production.
