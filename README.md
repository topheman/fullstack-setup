# fullstack-setup

This is a research repo that aims to answer [this issue (topheman/docker-experiments#1)](https://github.com/topheman/docker-experiments/issues/1).

Imagine you have a fullstack project with multiple technologies setup like:

- frontend (JavaScript, with frameworks like React or Vue)
- backend (php, golang or whatever)
- ...

This project aims to describe a project organization of frontend / backend:

- not in the same language (not both in JavaScript)
- with linting for frontend
- with precommit hooks (husky)
- with full IDE integration of plugin use (such as eslint-plugins) with no more than a `yarn install`

## Prerequisites

- Node
- yarn

## Install

```shell
git clone https://github.com/topheman/fullstack-setup.git
cd fullstack-setup
yarn
```

This will also make the install inside `./sub-project` folder.

### Why use Yarn

A specific version of yarn is shipped with the repo in the `./bin` folder. With [.yarnrc](.yarnrc), whatever version of yarn your team members have on their local machine, they will all use this specific one.

This ensures consistency with reproducible installs, using `yarn.lock` with the exact same version of `yarn`.

## Commands

Please check both:

- [package.json](./package.json)
- [./sub-project/package.json](./sub-project/package.json)

You'll see that npm task are runnable from the root of the project as well as inside the specifice folder. If we had multiple sub-projects (like frontend, backend ...), we could run both from the top.

## Run

```shell
npm start
```

## Build

```shell
npm run build
```

## Test

```shell
npm test
```
