# ProbeRequestForm <!-- omit in toc -->

- [Getting Started](#getting-started)
  - [Step 0 - Recommended IDE Setup](#step-0---recommended-ide-setup)
  - [Step 1 - Local Development Prerequisite](#step-1---local-development-prerequisite)
  - [Step 2 - Clone Repository](#step-2---clone-repository)
  - [Step 3 - Install Dependencies](#step-3---install-dependencies)
  - [Step 4 - Run application locally in development mode](#step-4---run-application-locally-in-development-mode)
- [Scripts](#scripts)
- [Pre-commit Hooks](#pre-commit-hooks)
  - [About Pre-commit Hooks](#about-pre-commit-hooks)
  - [Bypassing Pre-commit Hooks](#bypassing-pre-commit-hooks)
- [Code scaffolding](#code-scaffolding)
- [Storybook](#storybook)
- [Testing](#testing)
  - [Jest](#jest)
  - [Angular Testing Library](#angular-testing-library)
  - [Testing Library Jest DOM](#testing-library-jest-dom)
  - [TODO: Testing Library User Event](#todo-testing-library-user-event)
  - [TODO: Test Organization](#todo-test-organization)
  - [Run Tests](#run-tests)
  - [Debug Tests In VS Code Debugger](#debug-tests-in-vs-code-debugger)
  - [View Test Coverage](#view-test-coverage)
  - [Test Coverage Ignore Lines or Files](#test-coverage-ignore-lines-or-files)
- [CI/CD Pipeline Notes](#cicd-pipeline-notes)
  - [TODO: Environment Variables](#todo-environment-variables)
  - [Build Pipelines](#build-pipelines)
  - [Release Pipelines](#release-pipelines)
  - [TODO: Versioning](#todo-versioning)
  - [TODO: Hot fixes](#todo-hot-fixes)
- [Icons](#icons)
- [ESLint and Prettier](#eslint-and-prettier)
  - [What is ESLint](#what-is-eslint)
  - [What Is Prettier](#what-is-prettier)
  - [Linting \& Prettier Disable Conventions](#linting--prettier-disable-conventions)
  - [Eslint Ignore Node](#eslint-ignore-node)
  - [Prettier Ignore Node](#prettier-ignore-node)
  - [Ignore root files or directories](#ignore-root-files-or-directories)
- [Extra Notes](#extra-notes)
  - [Screen Dimensions Reference Table](#screen-dimensions-reference-table)
  - [Font Styling \& REM Reference Table](#font-styling--rem-reference-table)

## Getting Started

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 15.1.1.

### Step 0 - Recommended IDE Setup

- Install [VSCode](https://code.visualstudio.com/)
- Add these VSCode Extensions:

  - [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) - Provides immediate linting when writing code.
  - [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) - Used to automatically format code files to a consistent style.
  - [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph) - View a Git Graph of your repository, and easily perform Git actions from the graph.
  - [Markdown All In One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) - Useful for managing table of contents in markdown files. Also provides other useful features.
  - [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) - linting for markdown files to encourage standards and consistency for Markdown files.
  - [open in browser](https://marketplace.visualstudio.com/items?itemName=techer.open-in-browser) - Useful to quickly open [test coverage](#view-test-coverage) files in browser.

### Step 1 - Local Development Prerequisite

- Install git using [these instructions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
- Install Node 18+
  - **Mac/Linux**: [Node Version Manager](https://github.com/nvm-sh/nvm)
  - **Windows 10/11**: [Node Windows Installer](https://nodejs.org/en/)

### Step 2 - Clone Repository

Run the following command:

```terminal
git clone https://aerobt.visualstudio.com/AppDevUI/_git/ProbeRequestForm
```

### Step 3 - Install Dependencies

Run the following commands:

```terminal
npm install
```

### Step 4 - Run application locally in development mode

Run the following command:

```terminal
npm start
```

## Scripts

`ng` - Angular CLI command

`npm run start` - Runs the app in development mode. Open <http://localhost:4200/> to view it in the browser. The page will reload if you make edits.

`npm run start:acd` - Runs the app in development mode using the "acd-index.html" page. This serves as an example of how the app will function within the ACD site, while allowing development locally as `npm run start` does.

`npm run build` - Builds the app for production.

`npm run build:acd` - Builds the app for production with output hashing turned off and uses the root "acd-index.html" page as the base page for the application.

`npm test` - Launches the test runner in the interactive watch mode and includes test coverage information.

`npm run test:nowatch` - Launches the test runner once and exits. Tests will NOT rerun when something changes.

`npm run lint` - Run ESLint

`npm run lint:fix` - Run ESLint and fix automatically fixable problems.

`npm run lint:check` - Run ESLint and exit with an error status if there are any errors or warnings.

`npm run prettier` - Format files to conform to the Prettier Style Guide.

`npm run prettier:check` - Check if files conforms to the Prettier Style Guide without making changes. Exits with an error status if files require re-formatting.

`npm run storybook` - Builds and runs storybook component documentation for development.

`npm run storybook:build` - Builds storybook component documentation for deployment

`npm run prepare` - Script that automatically runs after `npm install`. This will setup pre-commit hooks.

## Pre-commit Hooks

### About Pre-commit Hooks

> ⚠️ IMPORTANT - Committing can seem to take a while if using the Git GUI in VS Code. This is because the linting and testing is running in the background before the commit is executed. If you're committing in the terminal you'll see the pre-commit hooks running.

We use [Husky](https://typicode.github.io/husky/#/?id=features) to run linters, prettier, type checking, and tests before code can be committed locally. This helps us keep our codebase clean and functioning; and it helps you to know sooner if your code does not meet the linting, code formatting, or testing standards.

To see what scripts are ran before code is committed you can look in the `./.husky/pre-commit` file.

TODO: add lint staged back into the project

### Bypassing Pre-commit Hooks

you can bypass `pre-commit` hooks using the `--no-verify` option. Example:

```shell
`git commit -m "yolo" --no-verify`
```

## Code scaffolding

Run the following to generate a new component:

```terminal
ng generate component component-name
```

You can also use

```terminal
ng generate directive|pipe|service|class|guard|interface|enum|module
```

## Storybook

We are using [Storybook 7.0 Angular](https://storybook.js.org/docs/7.0/angular/get-started/why-storybook) to help develop and document our components in isolation

## Testing

### Jest

[Jest](https://jestjs.io/docs/getting-started) is a testing framework we are using for this application.

### Angular Testing Library

We use [Angular Testing Library](https://testing-library.com/docs/angular-testing-library/intro/) to test our Angular components.
Testing Library encourages us to avoid testing [implementation details](https://kentcdodds.com/blog/testing-implementation-details); like the internals of a component we're testing (though it's still possible). The [Guiding Principles](https://testing-library.com/docs/guiding-principles) of this library emphasize a focus on tests that closely resemble how our web pages are interacted by the users.

### Testing Library Jest DOM

[Testing Library Jest DOM](https://testing-library.com/docs/ecosystem-jest-dom/) is a companion library for Testing Library that provides custom DOM element matchers for Jest

### TODO: Testing Library User Event

- fire event vs user event
- issue with long running tests with text input

### TODO: Test Organization

[Avoid Nesting when you're Testing](https://kentcdodds.com/blog/avoid-nesting-when-youre-testing)

### Run Tests

Run the following command to launch the test runner in interactive watch mode. It'll also provide test coverage information.

```terminal
npm test
```

### Debug Tests In VS Code Debugger

> ⚠️ IMPORTANT - Test coverage will not work when running tests in debug mode.

To run the VS Code Debugger, click the debug icon and select the JavaScript Debug Terminal button.

![Test Screenshot 1](docs/test-screenshot-1.png)

A terminal should open with the message "Debugger attached.". Set a breakpoint in the file you want to debug. Then run `npm test` in the debug terminal. Code execution will stop when the breakpoint is hit.

![Test Screenshot 2](docs/test-screenshot-2.png)

For more information see [VS Code Debugger Documentation](https://code.visualstudio.com/docs/editor/debugging).

### View Test Coverage

The test coverage report can be found at `./coverage/lcov-report/index.html`. This can be opened in the browser. Note that coverage reports are ignored by git, and are created when running `npm test`

### Test Coverage Ignore Lines or Files

This should be done sparingly and with purpose. Sometimes there are pieces of code that are not worth testing. Usually involves code needed to configure a third party package that is otherwise mocked in tests. TypeScript interface definitions are also pointless to test.

To ignore the next thing in the source-code (functions, if statements, classes, you name it):

```ts
/* istanbul ignore next */
```

To ignore an entire file or directory, open the `jest.config.ts` file and update the `coveragePathIgnorePatterns` array to include the file or folder you wish to ignore.

## CI/CD Pipeline Notes

### TODO: Environment Variables

> ⚠️ IMPORTANT - This hasn't been done yet for this application since we have no environment variables.

For running the app locally or running tests, environment variables are set in the `.env` file respectively. For cloud environments (dev, qa, uat, prod) these environments are set in the release pipelines. The pipeline will search the code for strings that look like this `#{ ... }#` and replace them with the values set in the pipeline. We've added `src/app/config` files where all the strings are located, creating a single source of truth for the app to reference.

### Build Pipelines

There are 3 build pipelines. You can find them running here: <https://aerobt.visualstudio.com/AppDevUI/_build?definitionScope=%5CProbeRequestForm>. Build pipelines are defined in this project in the the `./pipelines` directory

The `pipelines/pr-azure-pipelines.yml` pipeline will run when a pull request into the `main` branch is published. It will prevent the PR from being completed until the following items pass:

- linting
- prettier
- unit tests
- storybook build
- app build

The `pipelines/ci-azure-pipelines.yml` pipeline will run when a pull request into `main` is completed. This will build the application and create an artifact for the static web app release pipeline to use.

The `pipelines/blob-azure-pipelines.yml` pipeline will run when a tag is created. This will build the application without hashing and create an artifact for the blob release pipelines to use.

### Release Pipelines

There are 2 release pipelines. You can find releases at the following link. Look in the `ProbeRequests` directory: <https://aerobt.visualstudio.com/AppDevUI/_release?_a=releases&view=all&path=%5CProbeRequestForm>

- One to deploy the application to a static website in each environment
- One to deploy the application in blob storage to be reference / used in other web applications

### TODO: Versioning

### TODO: Hot fixes

## Icons

As of 4/24/2023 the icons we use come from here: <https://heroicons.com/>

## ESLint and Prettier

### What is ESLint

[ESLint](https://eslint.org/) is a tool for identifying and reporting on patterns found in ECMAScript/JavaScript code, with the goal of making code more consistent and avoiding bugs.

Use the following command to run ESLint:

```terminal
npm run lint
```

Some parts of the code can be automatically fix. To automatically fix some ESLint errors run the following command:

```terminal
npm run lint:fix
```

### What Is Prettier

Prettier is used to format our code to conform to a consistent style.

### Linting & Prettier Disable Conventions

Please follow these 2 conventions When disabling a line or block of code:

**Convention 1** - Only disable the offending rule, not all of eslint. Example:

**Good** = `/* eslint disable no-console */`\
**Bad** = `/* eslint disable */`

**Convention 2** - Provide a note explaining why the rule is disabled

### Eslint Ignore Node

To disable a line of code do the following:

```js
// eslint-disable-next-line no-console
console.log("bar");
```

To disable a block of code do the following:

```js
/* eslint-disable no-console */

console.log("bar");

/* eslint-enable no-console */
```

### Prettier Ignore Node

In some cases prettier will reformat code that we don't want reformated. We can use `// prettier-ignore` to exclude the next node from formatting. For example:

```js
matrix(1, 0, 0, 0, 1, 0, 0, 0, 1);

// prettier-ignore
matrix(
  1, 0, 0,
  0, 1, 0,
  0, 0, 1
)
```

will be transformed to:

```js
matrix(1, 0, 0, 0, 1, 0, 0, 0, 1);

// prettier-ignore
matrix(
  1, 0, 0,
  0, 1, 0,
  0, 0, 1
)
```

### Ignore root files or directories

If a root file or directory needs to be ignored by ESLint or Prettier then add the file/directory name to the `.eslintignore` or `.prettierignore` files.

## Extra Notes

### Screen Dimensions Reference Table

| Name         | Dimensions  |
| ------------ | ----------- |
| Small Phone  | 375 x 667   |
| Large Phone  | 428 x 926   |
| Small Tablet | 768 x 1024  |
| Large Tablet | 1024 x 1366 |
| Laptop       | 1280 x 720  |
| Desktop      | 1920 x 1080 |
| QHD          | 2560 x 1440 |

### Font Styling & REM Reference Table

Use the [Golden Ratio Typography Calculator](https://grtcalculator.com/) to get recommendations on line height and content width given a font size.

REM Size can be calculated using the following equation: `Rem Size = (Desired Font size) / (HTML Font Size)`

**Example:** Assuming an HTML font size of 16px, then `12px / 16px = 0.75rem`

| REM Size | Pixel Size | Point Size |
| -------- | ---------- | ---------- |
| 0.75rem  | 12px       | 9pt        |
| 0.875rem | 14px       | 11pt       |
| 1.0rem   | 16px       | 12pt       |
| 1.125rem | 18px       | 14pt       |
| 1.25rem  | 20px       | 15pt       |
| 1.375rem | 22px       | 17pt       |
| 1.5rem   | 24px       | 18pt       |
| 1.625rem | 26px       | 20pt       |
| 1.75rem  | 28px       | 21pt       |
| 1.875rem | 30px       | 23pt       |
| 2.0rem   | 32px       | 24pt       |
| 2.125rem | 34px       | 26pt       |
| 2.25rem  | 36px       | 27pt       |
| 2.375rem | 38px       | 29pt       |
| 2.5rem   | 40px       | 30pt       |
| 2.625rem | 42px       | 32pt       |
| 2.75rem  | 44px       | 33pt       |
| 2.875rem | 46px       | 35pt       |
| 3.0rem   | 48px       | 36pt       |
