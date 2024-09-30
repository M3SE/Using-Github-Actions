# Using Github Actions

## Overview
This assignment entails practicing using Github Actions for automating continuous integration
(CI) and deployment (CD) workflows in software development projects.


### Key Points in the Documentation:
- **Purpose**: Describes the goal of the CI/CD pipeline and why it uses Docker.
- **Steps**: Breaks down each step in the workflow file, explaining what it does.
- **Configurations**: Lists any necessary GitHub secrets and provides an example Dockerfile.
- **Dependencies**: Highlights the need for Docker Hub credentials and the Dockerfile in your repository.

# CI/CD Workflow with Docker

## Purpose

This repository contains a Continuous Integration (CI) and Continuous Deployment (CD) pipeline using **GitHub Actions** with **Docker**. The purpose of this workflow is to automate the process of building, testing, and optionally deploying the application inside a Docker container, ensuring consistency across environments.

### Key Features:
- **CI Workflow**: Automatically triggered on every push or pull request to the `main` branch. It builds the Docker image, runs tests inside the container, and verifies the application.
- **CD Workflow (Optional)**: After successful testing, the Docker image is pushed to Docker Hub for deployment to any platform or server that supports Docker.

## Workflow Steps

### CI Workflow

The CI workflow runs on every push or pull request to the `main` branch and consists of the following steps:

1. **Checkout Code**:
   - Uses the `actions/checkout@v2` GitHub Action to check out the code from the repository.
   - This ensures the pipeline is working with the latest version of the code.
   
   ```yaml
   - name: Checkout code
     uses: actions/checkout@v2

