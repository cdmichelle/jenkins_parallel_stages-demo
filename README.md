# Jenkins Parallel Stages CI/CD Pipeline

This repo showcases a Jenkins Declarative Pipeline designed to optimize CI/CD workflows by leveraging **parallel stages**. The goal is to reduce overall build time and speed up feedback loops, which are critical for maintaining high development velocity and quality.

---

## Overview

The pipeline simulates a typical CI/CD process where linting, unit tests, and security scans run **concurrently**, cutting down wait times and allowing faster detection of issues. After these quality gates, the pipeline proceeds to build and deploy stages, providing a full delivery workflow example.

Key highlights:

- Runs linting, testing, and security scanning simultaneously to save time

- Simulates build and deployment to mimic real-world release pipelines

- Demonstrates practical use of Jenkins parallelism to improve pipeline throughput and reliability

---

## Pipeline Breakdown

### 1. **Checkout**

Pulls the latest source code from version control to ensure the pipeline runs against the newest changes.

### 2. **Parallel Quality Checks**

Executes three critical validation steps in parallel:

- **Linting**: Uses Flake8 style checks to enforce code quality.

- **Unit Testing**: Runs Python tests with Pytest to verify functionality.

- **Security Scanning**: Simulates vulnerability scanning (e.g., via Trivy) to catch potential security risks early.

### 3. **Build**

Simulates packaging or container image creation, preparing the app for deployment.

### 4. **Deploy**

Represents deployment to staging or production environments, closing the CI/CD loop.

---

## Tech Stack

| Tool/Tech | Purpose |

|---------------------|-----------------------------------|

| Jenkins | Pipeline orchestration and automation |

| Shell scripting | Command execution within stages |

| Python | Sample app and testing scripts |

| Pytest | Unit testing framework |

| Flake8 | Linting tool |

| Trivy | Container security scanner simulation |

---

## Project Structure