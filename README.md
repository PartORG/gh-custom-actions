# PartORG/gh-custom-actions

**Automate Your GitHub Actions with Custom Scripts**

[![JavaScript](https://img.shields.io/badge/language-JavaScript-blue.svg)] [![React](https://img.shields.io/badge/framework-React-green.svg)] [![License](https://img.shields.io/github/license/PartORG/gh-custom-actions)] [![Tests](https://img.shields.io/github/actions/workflow/status/PartORG/gh-custom-actions/test.yml?branch=main&label=tests)] [![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-Deploy%20to%20S3-blue.svg)]

## Introduction

`gh-custom-actions` is a collection of custom GitHub Actions workflows designed to automate various tasks in your repository. This project leverages React and TypeScript to create reusable components and utilities for automating common GitHub operations.

### Primary Workflow

The primary workflow involves deploying applications to AWS S3 using GitHub Actions. The project includes multiple actions, each tailored for different deployment scenarios:

- **Docker Deployment**: Deploys a Docker container to an S3 bucket.
- **JavaScript Deployment**: Deploys JavaScript applications to an S3 bucket.

### Main Advantages

- **Modular Architecture**: Each action is designed as a modular component, making it easy to reuse and extend.
- **Extensive Testing**: The project includes comprehensive testing using Vitest and Jest to ensure reliability.
- **Easy Configuration**: All configuration is handled through environment variables and GitHub Actions workflows.

## Features

### Docker Deployment

The `deploy-s3-docker` action automates the deployment of a Docker container to an S3 bucket. It handles the following tasks:

- Builds the Docker image.
- Pushes the image to a registry.
- Deploys the image to an S3 bucket.

### JavaScript Deployment

The `deploy-s3-javascript` action automates the deployment of JavaScript applications to an S3 bucket. It handles the following tasks:

- Bundles the application using Vite.
- Uploads the bundled files to an S3 bucket.

## How It Works

The project is structured as a monorepo with multiple GitHub Actions workflows. Each workflow is designed to handle specific deployment scenarios.

### Architecture Diagram

```plaintext
+-------------------+
|  GitHub Actions   |
+---------+---------+
          |
          v
+---------+---------+
|  Actions    |
+---------+---------+
          |
          v
+---------+---------+
|  Deployment Logic |
+---------+---------+
```

## Technology Stack

| Technology | Purpose |
|------------|---------|
| React      | Frontend framework for building user interfaces. |
| TypeScript | Static type checker that helps write robust JavaScript code. |
| Vite       | Build tool for modern web projects. |
| Jest       | Testing framework for JavaScript applications. |
| Vitest     | Fast test runner for JavaScript and TypeScript. |

## Requirements

- Node.js 14 or higher
- npm 7 or higher

## Installation

To install the project, follow these steps:

```sh
git clone https://github.com/PartORG/gh-custom-actions.git
cd gh-custom-actions
npm install
```

## Configuration

The following environment variables are used by the actions:

- `AWS_ACCESS_KEY_ID`: AWS access key ID.
- `AWS_SECRET_ACCESS_KEY`: AWS secret access key.
- `S3_BUCKET_NAME`: Name of the S3 bucket.

These variables should be set in your GitHub repository settings under Secrets.

## Quick Start

To deploy a Docker container using the `deploy-s3-docker` action, run:

```sh
npm run dev
```

To deploy a JavaScript application using the `deploy-s3-javascript` action, run:

```sh
npm run build
```

## Usage

Here are some example commands and entry points discovered in the repository:

- **Dev Server**: `npm run dev`
- **Linting**: `npm run lint`
- **Build**: `npm run build`
- **Preview**: `npm run preview`
- **Testing**: `npm run test`

## Project Structure

```plaintext
.
├── .eslintrc.json
├── .github
│   ├── actions
│   │   ├── cached-deps
│   │   ├── deploy-s3-docker
│   │   ├── deploy-s3-javascript
│   ├── workflows
│   │   └── test.yml
├── package.json
└── src
```

## Development

The project uses Vite for development. To start the development server, run:

```sh
npm run dev
```

## Testing

Tests are written using Vitest and can be run with:

```sh
npm run test
```

## Limitations

- The project assumes AWS credentials are available in the environment.
- The deployment logic is specific to S3 and may need adjustments for other storage solutions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.