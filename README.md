# GitHub-CICD

# 🚀 Flask CI/CD Pipeline using GitHub Actions

## 📌 Project Overview

This project demonstrates the implementation of a **CI/CD (Continuous Integration and Continuous Deployment) pipeline** for a Python Flask application using GitHub Actions.

The pipeline automates:

* Dependency installation
* Running tests
* Building the application
* Deployment to staging and production environments

---

## 🛠️ Technologies Used

* Python 3.10
* Flask
* Pytest
* GitHub Actions

---

## 📂 Project Structure

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

## ⚙️ CI/CD Workflow Explanation

The pipeline is defined in:

```
.github/workflows/ci-cd.yml
```

### 🔄 Workflow Triggers

| Event             | Action                      |
| ----------------- | --------------------------- |
| Push to `main`    | Runs CI pipeline            |
| Push to `staging` | Runs CI + deploy to staging |
| Release creation  | Deploy to production        |

---

## 🔁 Workflow Stages

### 1️⃣ Install Dependencies

* Installs required Python packages using `pip`

### 2️⃣ Run Tests

* Executes test cases using `pytest`
* Ensures code quality before deployment

### 3️⃣ Build 

* Prepares the application after successful tests

### 4️⃣ Deploy to Staging

* Triggered when code is pushed to `staging` branch
* Simulates deployment to staging server

### 5️⃣ Deploy to Production

* Triggered when a release tag (e.g., `v1.0`) is created
* Simulates production deployment

---

## 🔐 Environment Secrets

The following secrets are configured in repository settings:

| Secret Name | Description                    |
| ----------- | ------------------------------ |
| STAGING_KEY | Used for staging deployment    |
| PROD_KEY    | Used for production deployment |

> Note: These are stored securely using GitHub Secrets.

---

## 🚀 How to Run the Pipeline

### ✅ Trigger CI (Main Branch)

1. Make a change in `main`
2. Commit changes
3. Go to **Actions tab** to view pipeline execution

---

### 🧪 Trigger Staging Deployment

1. Switch to `staging` branch
2. Make a small code change
3. Commit changes
4. Pipeline will deploy to staging

---

### 🌍 Trigger Production Deployment

1. Go to **Releases**
2. Click **Create new release**
3. Add tag (e.g., `v1.0`)
4. Publish release
5. Production deployment will run automatically

---

## 📸 Screenshots

### ✅ Successful CI Pipeline

*(Add screenshot here)*

### 🧪 Staging Deployment

*(Add screenshot here)*

### 🌍 Production Deployment

*(Add screenshot here)*

---

## 🎯 Key Learning Outcomes

* Understanding CI/CD concepts
* Automating workflows using GitHub Actions
* Writing and running tests using pytest
* Managing branches (`main` and `staging`)
* Using GitHub Secrets for secure deployments



---

## 👨‍💻 Author

* Your Name : Sweta Patil
