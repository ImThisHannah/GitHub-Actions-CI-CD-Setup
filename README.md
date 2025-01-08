# GitHub-Actions-CI-CD-Setup

## What is it?

This is a CI/CD pipeline using GitHub Actions to run the component tests via Cypress when a Pull Request is made to the `develop` branch, and the application is deployed when code is merged from `develop` to the `main` branch.

## User Story
```md
AS A developer looking to integrate a pipeline in a codebase for continuous integration and deployment, 
I WANT to create a GitHub Action that will follow best practices by running test cases when a Pull Request is made to the develop branch
SO THAT I can ensure that all code integrations are clean and pass the proper requirements.

AS A developer looking to deploy the application automatically to Render when code is merged from develop to main,
I WANT to create a GitHub Action that will run when the code is merged to main and automatically deploys to Render
SO THAT the application is constantly updated when major releases are made to the main branch.
```
## Getting Started

You'll first upload the content inside the `Develop` folder to a GitHub Repository. 

You'll then deploy the application via [Render and MongoDB]

Once you see the application has been deployed, you'll navigate to the Settings option and turn off Auto-Deploy.

![Render image of auto deploy and hook](./Assets/19-Render-Settings.png)

Copy the `Deploy hook` URL as you will need it to properly configure GitHub Actions to deploy to Render.

Next, create a `develop` branch (either on GitHub directly or via command-line) where all feature branches will be merged to.

> **note** Your feature branches should always be merged to the `develop` branch. Only the `develop` branch should be merged to the `main` branch.

You will want to have two separate `YAML` files: one configured to execute GitHub Actions for tests when a Pull Request is made to the `develop` branch and the other configured to execute GitHub Actions to automatically deploy to Render when `develop` is merged to `main` branch.
