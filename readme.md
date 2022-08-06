# doogu-slim

Slim package of [doogu](https://github.com/bent10/doogu).

- [Install](#install)
- [What includes?](#what-includes)
- [Shareable configs](#shareable-configs)
  - [`tsconfig`](#tsconfig)
  - [`eslint`](#eslint)
  - [`prettier`](#prettier)
- [Scripts](#scripts)
- [Contributing](#contributing)
- [Thank you](#thank-you)

## Install

```bash
npm i -D doogu-slim
```

## What includes?

This package contains the following dependencies, for development purposes:

- [Prettier](https://prettier.io/) – An opinionated code formatter
- [ESLint](https://eslint.org/) – Pluggable JavaScript linter
- ~~[SWC](https://swc.rs/) – An extensible Rust-based platform for the next generation of fast developer tools~~
- [Typescript](https://www.typescriptlang.org/) – A language for application-scale JavaScript
- ~~[Jest](https://github.com/avajs/ava) – A delightful JavaScript Testing Framework~~
- [chokidar-cli](https://www.npmjs.com/package/chokidar-cli) – Fast `cross-platform` command line utility to watch file system changes

## Shareable configs

The configuration file that can be use with other projects.

### `tsconfig`

Extending the shareable config for TypeScript in `tsconfig.json` file:

```json
{
  "extends": "doogu-slim/config/tsconfig.json"
}
```

### `eslint`

Extending the shareable config for ESLint in `package.json` file:

```json
{
  "name": "mypackage",
  "version": "1.0.0",
  "eslintConfig": {
    "extends": "./node_modules/doogu-slim/config/eslint.json"
  },
  "eslintIgnore": ["hello.ts", "world.ts"]
}
```

### `prettier`

Extending the shareable config for Prettier in `package.json` file:

```json
{
  "name": "mypackage",
  "version": "1.0.0",
  "prettier": "doogu-slim/config/prettier.json"
}
```

## Scripts

The commands that can be use in `package.json` file:

```json
{
  "name": "mypackage",
  "version": "1.0.0",
  "scripts": {
    "start": "npm run build && npm run watch",
    "watch": "chokidar \"src/*.ts\" -c \"npm run build\"",
    "lint": "tsc --noEmit && eslint \"./src\" --ext \".ts\" --cache --cache-location \"node_modules/.cache/.eslintcache\"",
    "build": "",
    "test": "",
    "coverage": ""
  }
}
```

## Contributing

We 💛&nbsp; issues.

When committing, please conform to [the semantic-release commit standards](https://www.conventionalcommits.org/). Please install `commitizen` and the adapter globally, if you have not already.

```bash
npm i -g commitizen cz-conventional-changelog
```

Now you can use `git cz` or just `cz` instead of `git commit` when committing. You can also use `git-cz`, which is an alias for `cz`.

```bash
git add . && git cz
```

## Thank you

A project by [Stilearning](https://stilearning.com) &copy; 2022.
