
# TestingPractices_RestAssured_Cucumber_API

![RestAssured](https://img.shields.io/badge/RestAssured-6DB33F?style=for-the-badge&logo=java&logoColor=white)
![Cucumber](https://img.shields.io/badge/Cucumber-23D96C?style=for-the-badge&logo=cucumber&logoColor=white)
![TestNG](https://img.shields.io/badge/TestNG-FF7300?style=for-the-badge&logo=testng&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)

## Table of Contents

1. [About the Project](#about-the-project)
2. [Features](#features)
3. [Installation](#installation)
4. [Configuration](#configuration)
5. [Usage](#usage)
6. [Folder Structure](#folder-structure)
7. [Dependencies](#dependencies)
8. [Reporting](#reporting)
9. [Contributing](#contributing)
10. [License](#license)

## About the Project

The **TestingPractices_RestAssured_Cucumber_API** framework is an API testing solution for the Petstore API, utilizing RestAssured for API interactions, Cucumber for BDD (Behavior-Driven Development), and TestNG for test execution. This framework tests essential API functionalities, such as adding, updating, retrieving, and deleting pets.

## Features

- **API Testing with RestAssured**: Provides methods for `GET`, `POST`, `PUT`, and `DELETE` requests.
- **Behavior-Driven Development**: Uses Cucumber with Gherkin syntax to define scenarios in a human-readable format.
- **Detailed Reporting**: Generates HTML and PDF reports using ExtentReports for comprehensive test results.
- **Test Automation**: Tests include critical API functionality for the Petstore, including adding new pets, updating pet info, and verifying responses.

### Scenarios Covered
- **Get Pet by ID**: Retrieves pet information by ID and checks for a 200 response.
- **Add New Pet**: Adds a new pet to the store and verifies the response data.
- **Update Pet Info**: Updates existing pet details, confirming the status change.
- **Delete Pet by ID**: Deletes a pet by ID and validates the deletion response.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/ChatGTHB/TestingPractices_RestAssured_Cucumber_API.git
   ```
2. **Open the project in IntelliJ IDEA**:
   - Go to **File > Open** and select the project folder.
   - Ensure the project is imported as a Maven project.
3. **Install Plugins** (optional for IntelliJ IDEA):
   - **Cucumber for Java** and **Gherkin** plugins for Cucumber syntax support.
   - Go to **File > Settings > Plugins** and search for the plugins to install.

## Configuration

- **cucumber.properties**: Configures Cucumber options. Located in `src/test/resources`.
- **extent.properties**: Configures ExtentReports settings. Located in `src/test/resources`.
  ```properties
  extent.reporter.spark.start=true
  extent.reporter.spark.out=test-output/SparkReport/Spark.html
  extent.reporter.pdf.start=true
  extent.reporter.pdf.out=PdfReport.pdf
  ```

## Usage

1. **Run Tests**:
   - To run tests with TestNG, right-click on `TestRunnerExtentReport` in the `runners` package and select **Run**.
   - Alternatively, use Maven from the command line:
     ```bash
     mvn clean test
     ```

2. **Generate Reports**:
   - Test results are generated in HTML (`test-output/SparkReport/Spark.html`) and PDF (`PdfReport.pdf`) formats.

## Folder Structure

```plaintext
TestingPractices_RestAssured_Cucumber_API/
│
├── src/
│   └── test/
│       ├── java/
│       │   ├── features/             # Cucumber feature files
│       │   │   └── PetstoreAPITests.feature
│       │   ├── pages/                # API interaction classes
│       │   │   └── APIPage.java
│       │   ├── runners/              # TestNG runner classes
│       │   │   └── TestRunnerExtentReport.java
│       │   ├── stepDefinitions/      # Step definitions for Cucumber
│       │       └── PetstoreAPISteps.java
│       └── resources/
│           ├── cucumber.properties   # Cucumber configuration
│           ├── extent.properties     # ExtentReports configuration
│           ├── postman/              # Postman collection for API tests
│           │   └── Petstore API Test.postman_collection.json
│           └── testng.xml            # TestNG suite configuration
├── target/                           # Build output
└── pom.xml                           # Maven configuration file
```

## Dependencies

Dependencies are managed in the `pom.xml` file. Key dependencies include:

- **RestAssured**: For making HTTP requests to test the API.
- **Cucumber Java & TestNG**: Cucumber for BDD and TestNG for managing test execution.
- **ExtentReports**: For generating detailed HTML and PDF reports.
- **SLF4J**: Simple Logging Facade for Java, used for logging during testing.

## Reporting

Test reports are stored in `test-output` and `testReports` directories. Reports generated include:

- **HTML Report**: Located at `test-output/SparkReport/Spark.html`.
- **PDF Report**: Available at `PdfReport.pdf`.

These reports include test results, system information, and details of each test scenario.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.