# React Component Library

[![Build status](https://badge.buildkite.com/90ff98db996bb137c5be1bdce666c4b1ce68a25b17af0a6a04.svg?branch=master)](https://buildkite.com/harvey/react-component-library)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

This project skeleton was created to help people get started with creating their own React component library using:

  <img align="left" alt="TypeScript" width="30px" src="https://user-images.githubusercontent.com/6031883/144184752-6ed32b67-f687-4801-a156-e066af43362d.png" />
  <img align="left" alt="Sass" width="30px" src="https://user-images.githubusercontent.com/6031883/144184606-e6080dc1-c0e5-4cff-960e-0327e1bea58e.png" />
  <img align="left" alt="Rollup" width="30px" src="https://user-images.githubusercontent.com/6031883/144184830-bb3a4c0d-0d83-4a52-860a-ba94dfb7460f.png" />


<br />
<br />

It also features:

- [Storybook](https://storybook.js.org/) to help you create and show off your components
- [Jest](https://jestjs.io/) and [React Testing Library](https://github.com/testing-library/react-testing-library) enabling testing of the components

[Check out here to see the component library in action ▸](https://manisuec.github.io/react-ts-lib-starter/)

This starter kit also includes template for [CONTRIBUTING](CONTRIBUTING.md).

## Credits

This starter kit is forked from [https://github.com/HarveyD/react-component-library](https://github.com/HarveyD/react-component-library). 
I have updated the pacakge versions and some more customisation to suit my style.


## Development
I recommend to use below folder structure for better scalability

```
src
 └──├── assets
    │   └── scss
    │       ├── typography.scss
    │       └── variables.scss
    ├── components
    │   └── TestComponent
    │       ├── TestComponent.scss
    │       ├── TestComponent.stories.tsx
    │       ├── TestComponent.test.tsx
    │       ├── TestComponent.tsx
    │       ├── TestComponent.types.ts
    │       └── index.ts
    ├── hooks
    ├── index.ts
    ├── services
    ├── store
    └── utils
```
### Testing

```
npm run test
```

### Building

```
npm run build
```

### Storybook

To run a live-reload Storybook server on your local machine:

```
npm run storybook
```

## Publishing

### Hosting via NPM

First, make sure you have an NPM account and are [logged into NPM using the `npm login` command.](https://docs.npmjs.com/creating-a-new-npm-user-account)

Then update the `name` field in `package.json` to reflect your NPM package name in your private or public NPM registry. Then run:

```
npm publish
```

The `"prepublishOnly": "npm run build"` script in `package.json` will execute before publish occurs, ensuring the `build/` directory and the compiled component library exist.


## Deploy Storybook to GitHub Pages

Install `gh-pages`

`npm install gh-pages --save-dev`

Edit `package.json` file and add 

`"homepage": "http://YOUR_GITHUB_USERNAME.github.io/REPO_NAME`

Add below scripts in `package.json` 

```
"scripts": {
    "predeploy": "npm run build-storybook",
    "deploy-storybook": "gh-pages -d storybook-static",
    "build-storybook": "build-storybook"
},
```

Run `npm run deploy-storybook` to successfully host Storybook on github pages. 