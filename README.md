## About the project 


The project is based on repositories that I worked on while attending '4testers_automaty' test automation course
and is being maintained and extended by me for upskilling in test automation. 

This repository contains some basic UI and API tests of a simple web application.

## How to launch the app under test?

Tests can be run after cloning the following [web application](https://github.com/JacekStrzelecki/jstrzelecki_tested_app.git) repository.

The application is created in Docker environment, so before running tests you need to instantiate the application 
locally by following below instructions:

1. Install and launch Docker Desktop
2. In Terminal, change directory to the one where the tested app is located:

    ```cd /Users/<your_home_directory>/PycharmProjects/jstrzelecki_tested_app```

3. To run Docker containerized applications execute the below command:

    ```docker-compose up```

4. The status of the application can be checked with the following command:

   ```docker ps```

5. You can also check if the app works by running the below verification script:

    ```./run-docker-compose.sh```

6. The app is available under the http://localhost:8081/ address

credentials are: admin:admin

Swagger:

http://localhost:4001/swagger-ui.html

7. After finishing testing, stop running containers by executing the below command: 

    ```docker-compose down```

## What's in the repository?
 
'.github' folder:
This directory contains a YAML file that defines GitHub Actions workflows used for CI/CD processes.

'pages' folder:
In this directory you can find page object model classes used for UI testing using Selenium. 

'api', 'components' and 'generators' folders:
Utils for API/UI tests.

'tests' folder
Tests scripts. There are separate subfolders for UI and API tests.
Fixtures can be found in conftest.py file.

.env file:
The file contains variables for the tested app.

pytest.ini:
This is a configuration file for pytest framework.

requirements.txt file:
The files collects the list of external libraries.


## Allure

The project should deploy allure report to github pages. The report is generated from test execution job.

To run allure report locally use the following command:

```
allure serve allure-results
```

