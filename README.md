# Trunk-Based Development Git Strategy

## Overview

The Trunk-Based Development Git Strategy is a version control approach designed for development teams to maintain a single major branch (commonly referred to as `main`). 
This strategy encourages team members to frequently commit small changes directly to the main branch or to create optional short-lived feature branches. 
The primary goal is to enable rapid and continuous integration of code changes.

### Branch Structure

- **Main Branch**: 
  - This branch holds the production-ready code that is deployed to users. It represents the most stable version of the software and should always be in a deployable state.

- **Feature Branches**: 
  - Feature branches are created from the main branch to work on new features or improvements. Once development on a feature is complete, the feature branch is merged back into the main branch.

## Task Overview

In this lab, I will use the Trunk-Based Development Git Strategy to manage a production environment that relies solely on the main branch for production-ready code. 
I will also create optional feature branches that will be merged directly back into the main branch. By the end of this lab, you will gain a deeper understanding of how to effectively handle project changes using the Trunk-Based Development Git Workflow Strategy and its key concepts.

## Lab Objectives

By the end of this lab, learners will:

- Understand how to implement the Trunk-Based Development Git Workflow Strategy to manage a software project.
- Learn and practice fundamental Git commands such as branching, merging, and pushing.
- Gain proficiency in managing merging or committing directly into a linear branch.

## Getting Started

1. **Clone the Repository**: 
   ```bash
   git clone https://github.com/Dilys-web/Dilys_Opoku_Donkor_trunk_based_git_workflow_lab.git
   ```
2. **Navigate to the Project Directory**:
  ```bash
  cd <project-directory>
  ```
3. **Create a Feature Branch (if needed)**:
  ```bash   
  git checkout -b feature/your-feature-name
  ```
4. **Make Changes**:
  Edit files as needed, then stage and commit your changes:
  ```bash
  git add <file>
  git commit -m "Description of changes"
  ```
5. **Merge Changes Back to Main**:
   Switch to the main branch:
  ```bash
    git checkout main
  ```
6. **Merge the feature branch**:
  ```bash
  git merge feature/your-feature-name
  ```
7. **Push Changes to Remote Repository**:
  ```bash
  git push origin main
  ```
## Conclusion
   By following the Trunk-Based Development Git Strategy, teams can achieve a streamlined workflow that enhances collaboration and ensures that the codebase remains stable and ready for deployment. 
   This lab will provide you with the foundational skills necessary to implement this strategy effectively in your software projects.
