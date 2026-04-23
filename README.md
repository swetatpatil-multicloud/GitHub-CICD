# GitHub-CICD

# Flask CI/CD Pipeline using GitHub Actions

## Project Overview

This project demonstrates the implementation of a **CI/CD (Continuous Integration and Continuous Deployment) pipeline** for a Python Flask application using GitHub Actions.

The pipeline automates:

* Dependency installation
* Running tests
* Building the application
* Deployment to staging and production environments

---

## Technologies Used

* Python 3.10
* Flask
* Pytest
* GitHub Actions

---

## Project Structure

```
.
├── .github/workflows/
│   └── ci-cd.yml        # CI/CD pipeline configuration
├── app.py               # Flask application
├── test_app.py          # Test cases using pytest
├── requirements.txt     # Project dependencies
├── README.md            # Project documentation
```

---

## CI/CD Workflow Explanation

The pipeline is defined in:

```
.github/workflows/ci-cd.yml
```

### Workflow Triggers

| Event             | Action                      |
| ----------------- | --------------------------- |
| Push to `main`    | Runs CI pipeline            |
| Push to `staging` | Runs CI + deploy to staging |
| Release creation  | Deploy to production        |

---

## Workflow Stages

### Install Dependencies

* Installs required Python packages using `pip`

### Run Tests

* Executes test cases using `pytest`
* Ensures code quality before deployment

### Build 

* Prepares the application after successful tests

### Deploy to Staging

* Triggered when code is pushed to `staging` branch
* Simulates deployment to staging server

### Deploy to Production

* Triggered when a release tag (e.g., `v1.0`) is created
* Simulates production deployment

---

## Environment Secrets

The following secrets are configured in repository settings:

| Secret Name | Description                    |
| ----------- | ------------------------------ |
| STAGING_KEY | Used for staging deployment    |
| PROD_KEY    | Used for production deployment |

> Note: These are stored securely using GitHub Secrets.

---

## How to Run the Pipeline

### Trigger CI (Main Branch)

1. Make a change in `main`
2. Commit changes
3. Go to **Actions tab** to view pipeline execution

---

### Trigger Staging Deployment

1. Switch to `staging` branch
2. Make a small code change
3. Commit changes
4. Pipeline will deploy to staging

---

### Trigger Production Deployment

1. Go to **Releases**
2. Click **Create new release**
3. Add tag (e.g., `v1.0`)
4. Publish release
5. Production deployment will run automatically

---

### Successful CI Pipeline

<img width="940" height="322" alt="image" src="https://github.com/user-attachments/assets/fa38f096-031c-4501-835f-5cf96a79a230" />

### Staging Deployment

<img width="940" height="318" alt="image" src="https://github.com/user-attachments/assets/be1b3d12-da4a-49b2-8033-18bebdb84f6f" />

<img width="940" height="322" alt="image" src="https://github.com/user-attachments/assets/7ec0a8e1-71af-4411-928a-d14d5c2ad094" />

<img width="940" height="399" alt="image" src="https://github.com/user-attachments/assets/75f03a33-b230-4be8-97f4-1df0cedddf1c" />

<img width="619" height="849" alt="image" src="https://github.com/user-attachments/assets/65fbc03a-3acd-473b-8d26-6e62ea9426a1" />

<img width="672" height="558" alt="image" src="https://github.com/user-attachments/assets/4e4211f3-6406-42df-bcd1-051aab18ce74" />


### Production Deployment

<img width="940" height="411" alt="image" src="https://github.com/user-attachments/assets/e348ea58-57b6-4636-9cbf-52b15446f0a0" />

<img width="940" height="394" alt="image" src="https://github.com/user-attachments/assets/a076be89-9f6a-42e4-8c4c-c9f8f1b7c551" />

<img width="940" height="412" alt="image" src="https://github.com/user-attachments/assets/90a704f1-0a38-4483-9663-413c5f8440d9" />


## Key Learning Outcomes

* Understanding CI/CD concepts
* Automating workflows using GitHub Actions
* Writing and running tests using pytest
* Managing branches (`main` and `staging`)
* Using GitHub Secrets for secure deployments

## Author

* Your Name : Sweta Patil
