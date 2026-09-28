# AutomationProjectP01

A Selenium WebDriver automation testing project built using **Java, Selenium, TestNG, Maven, and Jenkins**.

The project demonstrates UI automation using the **Page Object Model (POM)**, reusable utilities, TestNG test execution, Maven build management, and CI execution through Jenkins.

---

## Project Status

The automation suite currently contains **7 UI test cases**.

- Local execution: **7/7 tests passed**
- Jenkins CI execution: **7/7 tests passed**
- Build tool: Maven
- Test framework: TestNG
- CI tool: Jenkins

## Tech Stack

* **Java 21**
* **Selenium WebDriver** 
* **TestNG**
* **Maven**
* **Jenkins**
* **Chrome Browser**
* **Page Object Model (POM)**
* **Git / GitHub**

---

## CI/CD Flow

GitHub → Jenkins → Maven → TestNG → Selenium WebDriver → Test Results

Code changes are pushed to GitHub and the Jenkins job checks out the
repository and executes the automated TestNG suite using Maven.

## Project Structure


AutomationProjectP01
│
├── src
│   ├── main
│   │   └── java
│   │       └── ...
│   │
│   └── test
│       └── java
│           └── ...
│
├── pom.xml
├── testng.xml
└── README.md



## Key Features

### 1. Page Object Model

The project follows the **Page Object Model** design pattern to separate:

* Page locators
* Page-specific actions
* Test execution logic

This improves code readability, maintainability, and reusability.

### 2. Explicit Waits

Explicit waits are used to wait for elements and page conditions rather than relying on fixed delays.

A reusable `WebUtilities` approach is used for common Selenium operations.

### 3. TestNG

TestNG is used for:

* Test execution
* Test organization
* Assertions
* Test suites
* Test reporting

### 4. Maven

Maven is used for:

* Dependency management
* Project build
* Test execution
* Surefire test reporting

Tests can be executed using:

```bash
mvn clean test
```

### 5. Jenkins CI

The project is integrated with Jenkins for continuous integration.

The Jenkins job executes:

```bash
mvn clean test
```

This allows the automation suite to be executed outside the local Eclipse environment and provides build/test results through Jenkins.

---

## Test Scenarios

The automation project contains UI test scenarios covering booking and
search workflows, including:

* Destination/search validation
* Date selection
* Guest and room selection
* Search execution
* Search result validation
* Hotel selection and reservation flow
* Booking details and guest field validation
* Negative/error validation scenarios
* Different currency/language combinations

Example test data includes:

* Yas Island — MYR / Bahasa Malaysia
* Auckland — INR / English

---

## Running the Project Locally

### Prerequisites

Make sure the following are installed:

* Java 21
* Maven
* Google Chrome
* Eclipse or another Java IDE

Verify Java:

```bash
java -version
```

Verify Maven:

```bash
mvn -version
```

### Clone the Repository

```bash
git clone https://github.com/testingproject2804/AutomationProjectP01
```

Navigate to the project directory:

```bash
cd AutomationProjectP01
```

Run the tests:

```bash
mvn clean test
```

---



## Jenkins Execution

The project is integrated with Jenkins for CI execution.

Jenkins checks out the project from GitHub and executes:

```bash
mvn clean test


## Test Execution Stability

Test execution can occasionally be affected by external factors such as:

* Network connectivity
* Website response time
* Browser/page loading time
* Temporary application delays
* Test environment conditions

Because the automation interacts with a live web application, an isolated test failure should be investigated by checking the failure reason and rerunning the suite before treating it as an application defect.

The project uses explicit waits to reduce synchronization-related failures.

---

## Reporting

Maven Surefire generates test execution reports after the test run.

Reports can be found under:


target/surefire-reports

These reports provide information about:

* Passed tests
* Failed tests
* Skipped tests
* Test execution details

---

## Framework Design

The framework follows a Page Object Model structure with reusable
utilities.

* **Page Objects** – Store page locators and page-specific actions
* **Base Test** – Handles WebDriver initialization and test setup/teardown
* **WebUtilities** – Provides reusable explicit-wait and Selenium utilities
* **Test Classes** – Contain test scenarios and assertions
* **Test Data** – Externalized test data is used for data-driven scenarios
* **TestNG** – Controls test execution and test suites


## Learning Objectives

This project is intended to demonstrate practical knowledge of:

* Selenium WebDriver
* Java automation
* TestNG
* Maven
* Page Object Model
* Explicit waits
* Test automation framework design
* Git/GitHub
* Jenkins CI execution
* Debugging and analyzing automation failures

---


```
