# New Project Checklist

- [ ] Install initial code (see the guides within this repo)
  - [ ] TODO: Create workspace recommended vs code extensions
- [ ] Replace default README with the example one found in the `./examples` directory
  - [ ] Change the header of that readme to the application name.
- [ ] Install and/or modify ESLint Config
  - [ ] TODO: Consider adding stylelint
- [ ] Install Prettier
- [ ] Install Storybook
- [ ] Add Tailwind CSS
  - [ ] Add Tailwind Prettier Plugin
  - [ ] TODO: something about tailwind intellisense for vscode
- [ ] Add UI Component Library
  - [ ] Configure Component Library Theme
  - [ ] look into primereact/primeng/primevue https://primetek.com.tr/#products
- [ ] Modify `package.json` `scripts`
  - [ ] `start`
  - [ ] `build`
  - [ ] `test`
  - [ ] `test:coverage`
  - [ ] `test:nowatch`
  - [ ] `test:check` (No watch and coverage flags enabled)
  - [ ] `lint`
  - [ ] `lint:fix`
  - [ ] `lint:check`
  - [ ] `prettier`
  - [ ] `prettier:check`
  - [ ] `storybook`
  - [ ] `storybook:build`
  - [ ] `prepare` (setup pre-commit hooks. TODO: does this work with yarn?)
- [ ] Setup CI/CD Pipeline
  - [ ] Add Husky and Lint stage pre commit hooks
  - [ ] Setup branch policies and PR status checks
    - [ ] lint
    - [ ] prettier
    - [ ] tests
    - [ ] build
  - [ ] Build and deploy to DEV
  - [ ] Pending approval deploy to QE
  - [ ] Pending approval deploy to UAT
    - [ ] TODO: Maybe require versioning assignment step somehow?
  - [ ] Pending approval deploy to PROD
- [ ] ...
- [ ] Delete this section
