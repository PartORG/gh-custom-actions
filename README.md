# gh-custom-actions

A JavaScript-based project that leverages React and React DOM to build interactive user interfaces, with a focus on deploying applications using GitHub Actions workflows.

[![JavaScript](https://img.shields.io/badge/language-JavaScript-blue.svg)] [![React](https://img.shields.io/badge/react-18.2.0-green.svg)] [![License](https://img.shields.io/github/license/PartORG/gh-custom-actions)] [![GitHub Actions](https://github.com/PartORG/gh-custom-actions/workflows/Deploy%20to%20S3/badge.svg)] [![Vite](https://img.shields.io/badge/vite-3.0.7-green.svg)] [![ESLint](https://img.shields.io/badge/eslint-8.23.0-blue.svg)] [![Jest](https://img.shields.io/badge/jest-29.0.1-green.svg)]

## Introduction

`gh-custom-actions` is a project designed to demonstrate the use of React and React DOM for building user interfaces, along with GitHub Actions for continuous integration and deployment. The project uses Vite as the build tool, ESLint for linting, Jest for testing, and various other dependencies to ensure a robust development environment.

The primary workflow involves developing, building, previewing, and deploying the application using GitHub Actions workflows. This setup ensures that the application is continuously tested and deployed to S3, making it accessible via a web URL.

## Features

- **React and React DOM**: The core technologies used for building interactive user interfaces.
- **Vite**: A build tool that provides fast development server and efficient production builds.
- **ESLint with React Plugin**: Ensures code quality and adheres to coding standards specific to React components.
- **Jest**: For running unit tests, ensuring the application behaves as expected.
- **GitHub Actions Workflows**: Automates deployment processes using Docker and S3.

## How It Works

The project follows a typical development workflow:

1. **Development**: Use `npm run dev` to start the Vite development server.
2. **Linting**: Run `npm run lint` to check and fix code style issues.
3. **Building**: Execute `npm run build` to create production-ready assets.
4. **Previewing**: Use `npm run preview` to serve the built application locally.
5. **Testing**: Run `npm run test` to execute unit tests using Jest.

GitHub Actions workflows are configured to deploy the application automatically:

- **Deploy to S3**: Deploys the built application to an S3 bucket, making it accessible via a web URL.

## Technology Stack

| Technology | Purpose |
|------------|---------|
| React      | JavaScript library for building user interfaces. |
| React DOM  | Enables React to render in the browser. |
| Vite       | Build tool that provides fast development server and efficient production builds. |
| ESLint     | Linter for identifying and reporting on patterns found in ECMAScript/JavaScript code, with a focus on enforcing coding standards. |
| Jest       | JavaScript Testing Framework with a focus on simplicity and speed. |
| GitHub Actions | Automates deployment processes using Docker and S3. |

## Requirements

- Node.js 14 or later
- npm (Node Package Manager)

## Installation

To install the project dependencies, run:

```bash
npm install
```

## Configuration

The project uses environment variables for configuration. The following environment variables are observed:

- `REACT_APP_API_URL`: URL of the API endpoint.

Configuration files include:

- `.eslintrc.json`: ESLint configuration file.
- `package.json`: Project dependencies and scripts.

## Quick Start

To get started with the project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/PartORG/gh-custom-actions.git
   cd gh-custom-actions
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```

## Usage

To build and preview the application, use:

```bash
npm run build
npm run preview
```

To run tests:

```bash
npm run test
```

## Project Structure

The project structure is organized as follows:

```
gh-custom-actions/
├── .eslintrc.json
├── node_modules/
├── public/
│   └── index.html
├── src/
│   ├── assets/
│   ├── components/
│   ├── App.jsx
│   ├── index.jsx
│   └── vite-env.d.ts
├── .gitignore
├── package.json
└── vite.config.js
```

- `src/`: Contains the source code of the application.
- `public/`: Contains static assets like HTML and images.
- `.eslintrc.json`: ESLint configuration file.
- `package.json`: Project dependencies and scripts.

## Development

The development workflow involves using Vite for development, building, and previewing. ESLint is configured to enforce coding standards with a focus on React components. Jest is used for unit tests. GitHub Actions includes workflows for deploying the application using Docker and S3.

## Testing

Unit tests are run using Jest:

```bash
npm run test
```

## Limitations

- The project assumes a specific environment setup.
- Deployment to S3 requires proper configuration of AWS credentials.

## License

This project is licensed under the [MIT License](LICENSE).