# Python CI/CD Pipeline with Jenkins

A beginner-friendly CI/CD project that demonstrates how to automate the execution, testing, and code coverage analysis of a Python calculator application using **Jenkins, Groovy, GitHub, and Pytest**.

This project is part of my hands-on learning journey in **DevOps and CI/CD automation**, where I explore how different tools work together to simplify software development workflows.

## Project Overview

In this project, I connected a GitHub repository to Jenkins and created a declarative pipeline using a Groovy script.

The pipeline is divided into multiple stages, with each stage handling a specific task in the application workflow.

### Pipeline Workflow

```text
GitHub Repository
       |
       v
     Checkout
       |
       v
  Setup Python
       |
       v
Install Dependencies
       |
       v
 Run Application
       |
       v
   Run Tests
       |
       v
 Test Coverage
       |
       v
 Build Artifacts
       |
       v
  Post Actions
```

## Technologies Used

| Technology | Purpose |
| ---------- | ----------------------------------- |
| Jenkins | CI/CD pipeline automation |
| Groovy | Writing the Jenkins Pipeline script |
| Python | Calculator application development |
| GitHub | Source code management |
| Pytest | Automated testing |
| pytest-cov | Test coverage reporting |
| Flake8 | Python code style checking |
| pip | Python dependency installation |

## Pipeline Stages

**1. Checkout**

Retrieves the Python application source code from the connected GitHub repository.

**2. Setup Python**

Prepares the Python environment required to run the application.

**3. Install Dependencies**

Installs the required Python packages using `requirements.txt`.

**4. Run Application**

Executes the Python calculator application through Jenkins and displays the results of basic arithmetic operations.

**5. Run Tests**

Runs automated unit tests using Pytest to check the calculator's addition, subtraction, multiplication, and division functions, including division-by-zero handling.

**6. Test Coverage**

Uses `pytest-cov` to measure how much of the application code is covered by the automated tests.

**7. Build Artifacts**

Handles the build artifact stage as part of the pipeline workflow.

**8. Post Actions**

Performs post-build tasks such as workspace cleanup and reports the pipeline result.

## Project Structure

```text
python-jenkins-demo/
│
├── app.py
├── test_app.py
├── requirements.txt
└── README.md
```

## How to Run This Project

### Prerequisites

- Python installed
- Jenkins installed and running
- Git installed
- GitHub account
- Required Jenkins pipeline support

### Step 1: Clone the Repository

```bash
git clone https://github.com/StevePillai/python-jenkins-demo.git
```

```bash
cd python-jenkins-demo
```

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 3: Run the Application

```bash
python app.py
```

### Step 4: Run Tests

```bash
pytest test_app.py -v
```

### Step 5: Check Test Coverage

```bash
pytest --cov=app --cov-report=term-missing
```

### Step 6: Configure Jenkins

1. Open your Jenkins dashboard.
2. Create a new Pipeline job.
3. Configure the pipeline script in the job's Pipeline section.
4. Connect your GitHub repository as the source of the application.
5. Save the configuration and trigger a build.
6. Monitor the pipeline stages and console output.

## What I Learned

Through this project, I gained hands-on experience with:

- Connecting GitHub repositories with Jenkins.
- Writing a Jenkins Pipeline using Groovy.
- Organizing CI workflows into individual stages.
- Automating Python dependency installation and application execution.
- Integrating automated tests into a pipeline.
- Understanding test coverage and build artifacts.
- Monitoring pipeline execution and reviewing build results.
- Understanding how CI/CD automation reduces repetitive manual work.

## Future Improvements

This project is a foundation for exploring more advanced CI/CD practices. Some improvements I would like to work on next include:

- Triggering builds automatically using GitHub webhooks.
- Integrating Docker to containerize the Python application.
- Adding automated Flake8 code quality checks to the pipeline.
- Improving test reporting and failure notifications.
- Exploring automated deployment.

## Connect With Me

I'm documenting my journey as I learn **DevOps, Cloud Computing, and Automation** through practical projects and experiments.

- **LinkedIn:** [Steve Pillai](https://www.linkedin.com/in/steve-pillai-607533249/)
- **GitHub:** [StevePillai](https://github.com/StevePillai)

If you find this project useful or have suggestions for improvement, feel free to explore the repository and share your feedback.

**Learning by building, breaking, debugging, and improving.**
