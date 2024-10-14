# UI Automation Project

This repository contains a UI Automation project that is designed to run automated tests across various operating systems, browsers, and configurations using Jenkins CI.

## Project Overview

The project is integrated with Jenkins and leverages various tools and plugins to automate the testing process for different features of the system. It supports the following capabilities:

- **Operating Systems**: Windows (10, 8.1, 8, 7) and macOS (Big Sur, Catalina, Mojave, High Sierra, Sierra, etc.)
- **Browsers**: Chrome, Firefox, Microsoft Edge, Safari, Internet Explorer (varies by OS)
- **Screen Resolutions**: Multiple resolutions are supported, such as `1920x1080`, `1366x768`, `1280x1024`, etc.
- **Test Features**: The system tests various application features like authentication, database access, query builders, API integration, and more.

## Key Features

- **Multi-Browser and Multi-OS Support**: Automatically test on different browsers and operating systems based on Jenkins parameters.
- **Jenkins Pipeline Integration**: Seamless integration with Jenkins for continuous integration and testing.
- **Parameterized Builds**: The build process is highly customizable with parameters for operating system, browser, version, and screen resolution.
- **Automated Test Execution**: The project uses Selenium for web UI automation and integrates with LambdaTest for cross-browser testing.
- **Groovy Scripts**: Custom Groovy scripts are used to handle dynamic parameter choices for OS, browser, and resolution configurations.
- **Build Artifacts**: ExtentReports and screenshots of failed tests are generated and stored during test runs.

## Prerequisites

- Jenkins installed and configured with the following plugins:
    - **Maven Integration Plugin**
    - **Rebuild Plugin**
    - **Uno-Choice Parameter Plugin**
    - **LambdaTest Plugin**
    - **Git Plugin**
- Java and Maven installed on Jenkins nodes.
- Configuration files for build, data, and remote driver settings (managed by Jenkins).

## How to Use

1. **Clone the repository**:
    ```bash
    git clone https://github.com/harivignesh0101/automation.git
    ```

2. **Configure Jenkins Job**:
    - Go to Jenkins and create a new Maven project.
    - Configure the project using the provided XML configurations or manually set parameters such as `jenkins_operating_system`, `jenkins_browser_name`, `jenkins_browser_version`, `jenkins_screen_resolution`, and more.

3. **Run Tests**:
    - Trigger the job with desired parameters (OS, browser, resolution).
    - Jenkins will handle the entire process, including build setup, test execution, and report generation.

4. **View Reports**:
    - Extent Reports and test results will be available after the Jenkins build completes. You can also check screenshots of failed tests.

## Customization

You can modify the following elements in the Jenkins job:

- **Operating Systems**: Customize the list of supported operating systems in the `uno-choice` script.
- **Browsers**: Modify the browser options and versions in the script.
- **Features**: Add or remove test features by updating the `jenkins_feature_list` parameter.

## License

This project is licensed under the MIT License.
