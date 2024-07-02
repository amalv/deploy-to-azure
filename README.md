# Deploy to Azure: A Vite React TypeScript Project

This project demonstrates how to deploy a Vite React TypeScript web application to Azure Static Web Apps. It uses GitHub Actions to manage multiple environments, allowing for the preview of changes in branches before merging them into the main branch.

## Overview

The application is built with React and TypeScript. The deployment process to Azure Static Web Apps is automated using a GitHub Actions workflow, which provides a seamless integration for CI/CD.

## Technology Stack & Features

- 📦 **React**: A JavaScript library for building user interfaces.
- 📘 **TypeScript**: A typed superset of JavaScript that compiles to plain JavaScript.
- ⚡ **Vite**: A modern frontend build tool that significantly improves the development experience.
- 🚀 **Azure Static Web Apps**: A service that automatically builds and deploys full stack web apps to Azure from a code repository.
- 🛠 **CI/CD**: Continuous Integration and Continuous Deployment with GitHub Actions for Azure Static Web Apps.

## GitHub Actions Workflow

The GitHub Actions workflow defined in `azure-static-web-apps-lively-mushroom-049881203.yml` automates the build and deployment process. It triggers on push events to the `main` branch and on pull request events, creating a unique preview environment for each pull request.

### Workflow Steps

1. **Checkout**: Checks out the source code.
2. **Build and Deploy**: Builds the application and deploys it to Azure Static Web Apps.
  - **App Location**: `/` - The source code path for the application.
  - **Api Location**: Not applicable for this project.
  - **Output Location**: `dist` - The directory where the built app content is stored.

### Preview Environments

For each pull request, a unique preview environment is created, allowing for the testing of changes in isolation. This ensures that the main application remains unaffected until changes are merged.

## Deployment to Azure

The deployment to Azure Static Web Apps is configured to use the `dist` directory as the output location for the built application. This setup is specified in the GitHub Actions workflow and aligns with the build configuration in `package.json`.

### Build Configuration

- **Build Command**: `tsc -b && vite build` - Compiles TypeScript files and then builds the application using Vite.
- **Dependencies**: Includes React, TypeScript, ESLint, and Vite among others, ensuring a robust development setup.

## Getting Started

To get started with this project:

1. Clone the repository.
2. Install dependencies with `bun install`.
3. Start the development server with `bun run dev`.
4. Build the project for production with `bun run build`.

## Conclusion

This project exemplifies a modern web application setup with React and TypeScript, automated deployment to Azure Static Web Apps, and the use of GitHub Actions for CI/CD and managing preview environments. 