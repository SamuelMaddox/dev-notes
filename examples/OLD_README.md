# Create React App Sample Readme <!-- omit in toc -->

- [Initial TODO List](#initial-todo-list)
- [Getting Started](#getting-started)
  - [Step 0 - Prerequisite](#step-0---prerequisite)
  - [Step 1 - Clone Repository](#step-1---clone-repository)
  - [Step 2 - Install Dependencies](#step-2---install-dependencies)
  - [Step 3 - Start The Application](#step-3---start-the-application)
  - [Step 5 - Start Storybook](#step-5---start-storybook)
  - [Step 6 - Read the Documentation](#step-6---read-the-documentation)
- [Scripts](#scripts)
- [Initial CI/CD Pipeline TODO List](#initial-cicd-pipeline-todo-list)
- [CI/CD Pipeline](#cicd-pipeline)
  - [CI/CD Documentation goes here](#cicd-documentation-goes-here)
- [Code Management](#code-management)
  - [Branch Naming Convention](#branch-naming-convention)
  - [Pull Request Checklist](#pull-request-checklist)
- [File Structure](#file-structure)
  - [Sample File Structure](#sample-file-structure)
  - [File Structure Conventions](#file-structure-conventions)
- [Testing](#testing)
  - [React Testing Library](#react-testing-library)
  - [Run Tests](#run-tests)
  - [View Test Coverage](#view-test-coverage)
- [Pre-commit Hooks](#pre-commit-hooks)
  - [About Pre-commit Hooks](#about-pre-commit-hooks)
  - [Bypassing Pre-commit Hooks](#bypassing-pre-commit-hooks)
- [ESLint and Prettier](#eslint-and-prettier)
  - [What is ESLint](#what-is-eslint)
  - [What Is Prettier](#what-is-prettier)
  - [Linting & Prettier Disable Conventions](#linting--prettier-disable-conventions)
  - [Eslint Ignore Node](#eslint-ignore-node)
  - [Prettier Ignore Node](#prettier-ignore-node)
- [Story Book](#story-book)
  - [Storybook & React Testing Library](#storybook--react-testing-library)
  - [Storybook Accessibility Tests](#storybook-accessibility-tests)
  - [How to Publish a Static Storybook Web Application](#how-to-publish-a-static-storybook-web-application)
- [Material UI](#material-ui)
  - [MUI CSS Baseline](#mui-css-baseline)
  - [MUI Styles](#mui-styles)
  - [MUI Icons](#mui-icons)
  - [MUI Typography](#mui-typography)
  - [MUI Themes](#mui-themes)
  - [MUI Date/Time Pickers & Day.js](#mui-datetime-pickers--dayjs)
- [Emotion Styled Components](#emotion-styled-components)
- [React Router](#react-router)
- [Helmet](#helmet)
- [Day.js](#dayjs)
  - [Documentation](#documentation)
  - [Why Not Moment.js?](#why-not-momentjs)
  - [Plugins](#plugins)
- [Advance](#advance)
- [Extra Notes](#extra-notes)
  - [Shared VS Code Settings](#shared-vs-code-settings)
  - [Debugging from VS Code](#debugging-from-vs-code)
  - [Recommended VS Code Extensions](#recommended-vs-code-extensions)
  - [React TypeScript Cheat Sheet](#react-typescript-cheat-sheet)
  - [Screen Dimensions Reference Table](#screen-dimensions-reference-table)
  - [Font Styling & REM Reference Table](#font-styling--rem-reference-table)
- [Notes For Designers](#notes-for-designers)
  - [Component Library](#component-library)
  - [Icon Library](#icon-library)
  - [Configure Theme](#configure-theme)
- [SCRUM Notes](#scrum-notes)
  - [Agile Manifesto](#agile-manifesto)
  - [Story Statuses](#story-statuses)
  - [Definition of Ready](#definition-of-ready)
  - [Definition of Done](#definition-of-done)

## Initial TODO List

Below is a list of things to do that template Create React App couldn't setup automatically. It is assumed that this section will be deleted once the TODO list is finished.

TODO: Create list

- [ ] Change the header of this readme to the application name.
- [ ] Complete [Initial CI/CD Pipeline TODO List](#initial-cicd-pipeline-todo-list)
- [ ] TODO: configure create-react-app proxy if needed (provide link to advance section below)
- [ ] TODO: configure environment variables if needed (provide link to advance section below)
- [ ] TODO: public folder stuff
- [ ] TODO: designer/theme stuff
- [ ] Update `src/Pages/Core/ForbiddenPage` and `src/Pages/Core/NotFoundPage` with improved designs
- [ ] Share with the designer everything included in the [Notes For Designers](#notes-for-designers) section

## Getting Started

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

### Step 0 - Prerequisite

- Install git using [these instructions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
- Install Node 16+ using [Node Version Manager](https://github.com/nvm-sh/nvm)(Mac/Linux) or the [Node Windows Installer](https://nodejs.org/en/)(Windows 10/11)

### Step 1 - Clone Repository

Run the following command:

```terminal
git clone <Repository Link>
```

### Step 2 - Install Dependencies

```terminal
npm install -g yarn
yarn set version berry
yarn install
```

### Step 3 - Start The Application

```terminal
yarn start
```

Open your web browser and go to [http://localhost:3000](http://localhost:3000) to view the app.

### Step 5 - Start Storybook

We use Storybook to help build UI modules & components. See the [Story Book](#story-book) section of this readme for more details.

TODO: How to start storybook

TODO: storybook a11y addon

### Step 6 - Read the Documentation

Be sure to read through the rest of this readme to understand all the tooling used to help developers build this application and keep our codebase clean.

## Scripts

**`yarn start`** - Runs the app in the development mode. Open [http://localhost:3000](http://localhost:3000) to view it in the browser. The page will reload if you make edits. You will also see any lint errors in the console.

**`yarn build`** - Builds the app for production to the `build` folder. It correctly bundles React in production mode and optimizes the build for the best performance. The build is minified and the filenames include the hashes.

**`yarn postinstall`** - This script is called by yarn after a `yarn install`. This will setup the cloned repository to use husky pre-commit hooks.

**`yarn test`** - Launches the test runner in the interactive watch mode.

**`yarn test:coverage`** - Launches the test runner in the interactive watch mode and includes test coverage information.

**`yarn test:verbose`** - Launches the test runner in the interactive watch mode and displays individual test results with the test suite hierarchy.

**`yarn test:nowatch`** - Launches the test runner once and exits. Tests will **NOT** rerun when something changes.

**`yarn lint`** - Run ESLint.

**`yarn lint:fix`** - Run ESLint and fix automatically fixable problems.

**`yarn lint:check`** - Run ESLint and exit with an error status if there are any warnings.

**`yarn prettier`** - Format files to conform to the Prettier Style Guide.

**`yarn prettier:check`** - Check if files conforms to the Prettier Style Guide without making changes. Exits with an error status if files require re-formatting.

**`yarn storybook`** - Start Storybook locally. Open [http://localhost:6006](http://localhost:6006) to view it in the browser.

**`yarn build-storybook`** - Build Storybook as a static web application.

## Initial CI/CD Pipeline TODO List

This section blah blah blah is expcted to be deleted once complete, tasks to use everything seen below

- [ ] Setup Skeleton CI/CD Pipeline to deploy to a dev environment
- [ ] Setup Skeleton CI/CD Pipeline to deploy storybook (TODO: link on how to publish storybook in below section)
- [ ] Setup PR Status Checks
  - [ ] TODO: `yarn test:nowatch`
  - [ ] TODO: `yarn lint:check`
  - [ ] TODO: `yarn prettier:check`
  - [ ] TODO: Has enough reviews
- [ ] TODO: blah blah blah
- [ ] TODO: blah blah blah
- [ ] TODO: blah blah blah
- [ ] Write CI/CD documentation in the [CI/CD Pipeline](#cicd-pipeline) section

## CI/CD Pipeline

### CI/CD Documentation goes here

TODO: What CI/CD pipeline technologies are used?

TODO: Where can I view the status of our pipelines?

TODO: Where can I configure our pipeline? Where can I learn how to configure our pipeline?

TODO: Where can I view the published version of storybook? (TODO: link on how to publish storybook in below section)

TODO: See the Create React App documentation about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

TODO: [Continuous integration](https://create-react-app.dev/docs/running-tests/#continuous-integration)

## Code Management

### Branch Naming Convention

Branching follows the [gitflow workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow).

- `master`
- `hotfix-{version with patch number increased}`
- `release-{version with min or max number increased}`
- `develop`
- `feature-{id}-{name}`
- `story-{id}-{name}`
- `task-{id}-{name}`

### Pull Request Checklist

- [ ] Story/Task acceptance criteria has been met.
- [ ] Browser console is not displaying errors, warnings, or unnecessary console logs.
- [ ] There is no commented out or dead code.
- [ ] Names are semantic and meaningful.
- [ ] Code is clear and easy to understand.
- [ ] Code has no magic numbers. `./src/Utils/Core/Constants/TimeConstants.ts` are used where appropriate.
- [ ] Code Follows the DRY (Don't Repeat Yourself) principle.
- [ ] Code follows SOLID principles:
  - [ ] **Single Responsibility Principle** - Every Component/Objects/Function should have only one responsibility.
  - [ ] **Open Closed Principle** - Components/Objects/Functions should be open for extension, but closed for modification.
  - [ ] **Liskov Substitution Principle** - Every subclass or derived class should be substitutable for their base or parent class.
  - [ ] **Interface Segregation Principle** - A client should never be forced to implement an interface that it doesn’t use.
  - [ ] **Dependency Inversion Principle** - High-level module must not depend on the low-level module, but they should .depend on abstractions.
- [ ] Files follow the defined [File Structure](#file-structure) and the [File Structure Conventions](#file-structure-conventions).
- [ ] New Linting Disable comments follow the [Linting & Prettier Disable Conventions](#linting--prettier-disable-conventions).
- [ ] Modules/Components have [Story Book](#story-book) stories written.
- [ ] CSS styles are defined using using [Material UI Styles](#material-ui-styles) or [Emotion Styled Components](#emotion-styled-components).
- [ ] CSS styles are using values from the [Material UI Themes](#material-ui-themes) where applicable (palette, typography, shadows, transitions, zindex).
- [ ] Relative inks are implemented using [React Router](#react-router).
- [ ] Pages have [Helmet](#helmet) tags set.
- [ ] Dates use [Day.js](#dayjs) or have a good reason not to (Day.js is compatible with [MUI Date/Time Picker](https://mui.com/x/react-date-pickers/getting-started/#setup)).
- [ ] Tests are written to closely resemble how web pages are interacted with by the users.
- [ ] Tests avoid testing implementation details (in accordance with the [Testing Library Guiding Principles](https://testing-library.com/docs/#what-you-should-avoid-with-testing-library)).
- [ ] Test coverage is above 80%.
- [ ] Storybook a11y tests are passing (TODO: Link to storybook accessibility testing section)
- [ ] Linters are not throwing errors or warnings.
- [ ] Prettier has been ran.

TODO: time constants are using the constants defined in the utils

## File Structure

### Sample File Structure

```txt
📁 src
================================================================================
| 📁 API
| | 📁 FirstAPI
| | | 📄 index.ts
| | | 📄 Types.ts
================================================================================
| 📁 Components
| | 📁 Core
| | | 📁 FirstComponent
| | | | 📁 Assets
| | | | | 📄 icon.svg
| | | | 📁 Hooks
| | | | | 📄 UseFirstHook.ts
| | | | 📁 Utils
| | | | | 📄 FirstUtil.ts
| | | 📄 index.ts
| | | 📄 index.test.tsx
| | | 📄 Styles.ts
| | | 📄 Types.ts
================================================================================
| 📁 Config
| | 📁 FirstCategoryConfig
| | | 📄 OneFirstCategoryConfig.ts
| | | 📄 TwoFirstCategoryConfig.ts
| | | 📄 index.ts
| | | 📄 Types.ts
================================================================================
| 📁 Contexts
| | 📁 FirstContext
| | | 📄 index.ts
| | | 📄 Types.ts
================================================================================
| 📁 Font
| | 📁 FontName
| | | 📄 FontNameRegular.ttf
| | | 📄 FontNameItalic.ttf
| | | 📄 FontNameBold.ttf
| | | 📄 FontNameBoldItalic.ttf
| | 📄 FontName.css
================================================================================
| 📁 Hooks
| | 📁 UseFirstHook
| | | 📁 Utils
| | | | 📄 FirstUtil.ts
| | | 📄 index.ts
| | | 📄 Types.ts
================================================================================
| 📁 Layouts
| | 📁 MainLayout
| | | 📄 index.ts
| | | 📄 index.test.tsx
| | | 📄 Styles.ts
| | | 📄 Types.ts
================================================================================
| 📁 Modules
| | 📁 Layout
| | | 📁 MainHeader
| | | | 📁 Assets
| | | | | 📄 pic.png
| | | | 📁 Components
| | | | | ...
| | | | 📁 Hooks
| | | | | 📄 UseFirstHook.ts
| | | | 📁 Utils
| | | | | 📄 FirstUtil.ts
| | | | 📄 index.ts
| | | | 📄 index.test.tsx
| | | | 📄 Styles.ts
| | | | 📄 Types.ts
================================================================================
| 📁 Pages
| | 📁 Core
| | | 📁 HomePage
| | | | 📁 Assets
| | | | | 📄 pic.png
| | | | 📁 Hooks
| | | | | 📄 UseFirstHook.ts
| | | | 📄 index.ts
| | | | 📄 index.test.tsx
| | | | 📄 Styles.ts
| | | | 📄 Types.ts
================================================================================
| 📁 SharedAssets
| | 📁 GroupOne
| | | 📄 pic.png
================================================================================
| 📁 Types
| | 📁 GroupOne
| | | 📁 Classes
| | | | 📄 FirstClassType.ts
| | | 📁 Enums
| | | | 📄 FirstEnumType.ts
| | | 📁 Interfaces
| | | | 📄 FirstInterfaceType.ts
================================================================================
| 📁 Utils
| | 📁 Core
| | | 📁 Constants
| | | | 📄 TimeConstants.ts
| | | 📁 FirstUtil.ts
| | | | 📄 FirstUtil.ts
| | | | 📄 index.ts
| | | | 📄 Types.ts
| | 📁 TestUtils
| | | 📄 RenderPage.tsx
| 📄 App.test.tsx
| 📄 App.tsx
| 📄 index.css
| 📄 index.tsx
```

### File Structure Conventions

- Folders & Files in `/src` should use `PascalCase` for file names except for the following:

  - `/src/**/index.ext`
  - `/src/react-app-env.d.ts`
  - `/src/reportWebVitals.ts`
  - `/src/setupTests.ts`

- Folders in `/public` should use `PascalCase`, and files should use `camelCase`.

- The main code for a folder should be in a file sharing the same name as the folder. There should also be an `index.ts` file inside of that folder that is used to import then export the main code. This is to avoid having multiple files opened in your editor all named `index.ts` while also avoiding imports that look like `./ComponentName/ComponentName`.

- The top level `Components` folder should be for generic, used anywhere components (Like`HamburgerButton`, `SideNav`, `Input`). `Components` can have other `Components` as children.

- The top level`Modules` are really big (epic or feature level) components made up of smaller components. `Modules` can have other `Modules` and `Components` as children. The hope is that individual `Modules` should not be aware of other sibling `Modules`. The `src/API`, `src/Contexts`, and `src/Hooks` should help facilitate the communication across sibling `Modules`.

- Types should be defined in the `/src/Types` directory with the following exceptions:

  - [Emotion Styled Components](#emotion-styled-components) Types can be saved in the same file as the styles are.
  - Types used exclusively for `./Utils/TestUtils` can be defined in the same file as the utility function.
  - TODO: Why do I have a ./Types.ts in most folders above? Do i needs types for props? should I use ./Types.ts for those and write an exception rule here? is there type checking/optional fields for props in typescript? what if local ./types.ts files were for types used only within that component, while the global ./Types folder is used for types that are shared across files?

## Testing

### React Testing Library

[React Testing Library](https://testing-library.com/docs/react-testing-library/intro/#the-problem)

### Run Tests

By default, Jest will only run the tests related to files changed since the last commit. To run tests use the following command:

```terminal
yarn test
```

To display individual test results with the test suite hierarchy run this command:

```terminal
yarn test:verbose
```

### View Test Coverage

> NOTE: Tests run much slower with coverage so it is recommended to run it separately from your normal workflow.

To create or update a test coverage report run the following command:

```terminal
yarn test:coverage
```

This will display coverage in the terminal. It will also create a coverage report at `./coverage/lcov-report/index.html`. This can be opened in the browser. Note that coverage reports are ignored by `git`

## Pre-commit Hooks

### About Pre-commit Hooks

> ⚠️ IMPORTANT - Committing can seem to take a while if using the Git GUI in VS Code. This is because the linting and testing is running in the background before the commit is executed. If you're committing in the terminal you'll see the pre-commit hooks running.

We use [Husky](https://typicode.github.io/husky/#/?id=features) and [Lint Staged](https://www.npmjs.com/package/lint-staged?activeTab=readme) to run linters, prettier, and tests before code can be committed locally. This helps us keep our codebase clean and functioning; and it helps you to know sooner if your code does not meet the linting, code formatting, or testing standards.

To see what scripts are ran before code is commited you can look in the `./.husky/pre-commit` file. Note that one of the commands that are ran is `yarn lint-staged`. This is defined in the `package.json` in it's own section called `lint-staged`.

### Bypassing Pre-commit Hooks

you can bypass `pre-commit` hooks using the `--no-verify` option. Example:

```shell
`git commit -m "yolo" --no-verify`
```

## ESLint and Prettier

### What is ESLint

[ESLint](https://eslint.org/) is a tool for identifying and reporting on patterns found in ECMAScript/JavaScript code, with the goal of making code more consistent and avoiding bugs.

Use the following command to run ESLint:

```terminal
yarn lint
```

Some parts of the code can be automatically fix. To automatically fix some ESLint errors run the following command:

```terminal
yarn lint:fix
```

### What Is Prettier

Prettier is used to format our code to conform to a consistent style.

### Linting & Prettier Disable Conventions

Please follow these 2 conventions When disabling a line or block of code:

**Convention 1** - Only disable the rule offending rule, not all of eslint. Example:

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

## Story Book

This project uses Storybook to help isolate React Components for development. See [Storybook Documentation](https://storybook.js.org/docs/react/get-started/introduction) for more information.

TODO: quick notes for how to run/use storybook

### Storybook & React Testing Library

TODO: https://storybook.js.org/addons/@storybook/testing-react

### Storybook Accessibility Tests

TODO: https://storybook.js.org/docs/react/writing-tests/accessibility-testing

TODO: https://storybook.js.org/docs/react/writing-tests/accessibility-testing#automate-accessibility-tests-with-test-runner

### How to Publish a Static Storybook Web Application

[Publish Static Storybook Documentation](https://storybook.js.org/docs/react/sharing/publish-storybook).

## Material UI

TODO: General MUI notes. What is MUI.

[Material UI Documentation](https://mui.com/material-ui/)

### MUI CSS Baseline

> ⚠️ IMPORTANT - The most notable change MUI makes is setting `box-sizing: border-box` globally.

Material UI includes it's own global reset, similar to `normalize.css`. See their [CSS Baseline Approach](https://mui.com/material-ui/react-css-baseline/#color-scheme) documentation for details.

### MUI Styles

TODO: Styles Notes

Something about [Emotion Styled Components](#emotion-styled-components) is probably needed here

### MUI Icons

TODO: This needs reviewed/edited

we prefer the use of svg icons over font icons. This means the `Icon` component probably doesn't work. Please see the [Library of Icons](https://mui.com/material-ui/material-icons/) for a list of icons we have available. To include custom SVG icons see the [SVG Icon](https://mui.com/material-ui/material-icons/) section of the Material UI Documentation

### MUI Typography

TODO: Call this component out. Show how to use it (and when to explicitly use the values defined in the theme instead)

https://mui.com/material-ui/react-typography/

### MUI Themes

TODO: Theme Config

something about how to configure theme (pallete/fonts) here. ask to add light/dark mode palletes and bonus points for color blind palletes.

TODO: Explain how to remove the default Roboto font if you want to use a custom font instead

### MUI Date/Time Pickers & Day.js

[Material UI's Date/Time Pickers](https://mui.com/x/react-date-pickers/getting-started/#setup) are compatible with [Day.js](#dayjs) date/time objects, and the Day.js dependency is already included in this project.

## Emotion Styled Components

[See Emotion Documentation](https://emotion.sh/docs/introduction)

## React Router

[See React Router Documentation](https://reactrouter.com/docs/en/v6)

## Helmet

[See React Helmet Async Documentation](https://www.npmjs.com/package/react-helmet-async)

## Day.js

### Documentation

[Day.js Documentation](https://day.js.org/docs/en/parse/parse)

### Why Not Moment.js?

In 2020 Moment.js declared itself a [legacy project in maintenance mode](https://momentjs.com/docs/#/-project-status/) and discourages developers from using the library in new projects going forward.

### Plugins

By default, Day.js comes with core code only and no installed plugin.

A plugin is an independent module that can be added to Day.js to extend functionality or add new features.

[Day.js Plugins](https://day.js.org/docs/en/plugin/plugin)

Example of using Day.js Plugins:

```js
import dayjs from "dayjs";
import isToday from "dayjs/plugin/isToday";

dayjs.extend(isToday);
```

## Advance

TODO: Write documentation here AND include todo item with link in the project setup section todo list
[environment](https://create-react-app.dev/docs/adding-custom-environment-variables/)

TODO: [Using HTTPS in Dev](https://create-react-app.dev/docs/using-https-in-development/)

TODO: maybe this is it's own section, or is moved to CI/CD pipeline section
[web vitals](https://create-react-app.dev/docs/measuring-performance)

TODO: Write documentation here but Include todo item with link in project setup todo list
[proxy](https://create-react-app.dev/docs/proxying-api-requests-in-development)

and maybe more stuff from the create react app docs

## Extra Notes

### Shared VS Code Settings

Some VS Code Settings are overwritten by a shared settings file found at `./vscode/settings.json`. This is mostly used to help keep code files consistent within the project. These settings will not affect settings for other projects.

### Debugging from VS Code

TODO: Debugging from VS Code [debugging in the editor](https://create-react-app.dev/docs/setting-up-your-editor/#debugging-in-the-editor)

### Recommended VS Code Extensions

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) - Provides immediate linting when writing code.
- [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph) - View a Git Graph of your repository, and easily perform Git actions from the graph.
- [Markdown All In One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) - Most useful for managing table of contents in markdown files. Also provides other useful features.
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) - linting for markdown files to encourage standards and consistency for Markdown files.
- [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles) - Changes VS Code's built-in markdown preview to match GitHub's styling.
- [open in browser](https://marketplace.visualstudio.com/items?itemName=techer.open-in-browser) - Useful to quickly open [test coverage](#view-test-coverage) files in browser.
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) - Used to automatically format code files to a consistent style.
- [TODO Highlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight) - Highlight TODO, FIXME and other annotations within your code.
- [vscode-styled-components](https://marketplace.visualstudio.com/items?itemName=styled-components.vscode-styled-components) - CSS Syntax highlighting and IntelliSense for styled-components. Seems to work for Emotion Styled Components as well

### React TypeScript Cheat Sheet

Here is a link to the [React TypeScript Cheat Sheet](https://react-typescript-cheatsheet.netlify.app/docs/basic/getting-started/basic_type_example)

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

## Notes For Designers

### Component Library

Share with the designer this link for the [Library of Material UI Components](https://mui.com/material-ui/)

### Icon Library

Share with the designer this link for the [Library of Icons](https://mui.com/material-ui/material-icons/)

### Configure Theme

TODO: These may be useful to reference:

- [Material UI Typography](#material-ui-typography)
- [Material UI Themes](#material-ui-themes)

TODO: add link

Work with a designer to configure the [Material UI Theme]() for the site, including color pallet and fonts. We recommend configuring at least a light mode and dark mode color pallet. Bonus points for adding more themes for color blindness.

TODO: Publish Storybook internally and share with designer

## SCRUM Notes

### Agile Manifesto

**INDIVIDUALS AND INTERACTIONS** --- over processes and tools\
**WORKING SOFTWARE** --- over comprehensive documentation\
**CUSTOMER COLLABORATION** --- over contract negotiation\
**RESPONDING TO CHANGE** --- over following a plan

That is, while there is value in the items on the right, we value the items on the left more.

### Story Statuses

- New -> Refine -> Estimate -> Hold (For Dependencies) -> Ready -> Active -> In QA -> Demo -> Done

### Definition of Ready

- Includes a clear statement of the business value.
- There are no outstanding questions or decisions required by the business.
- Dependencies have been identified
- We can reasonably expect to complete the story and it's outstanding dependencies within the sprint
- Has acceptance criteria defined.
- Has an estimate.

### Definition of Done

- Story meets all acceptance criteria.
- Code meets all criteria defined in the [Pull Request Checklist](#pull-request-checklist).
- Code has been peer reviewed by at least 2 other developers.
- Code has been deployed to QA.
- Code has been tested and signed off by QA.
- Story has been demoed to and signed off by the Product Owner (if it is a non technical story).
