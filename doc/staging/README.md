# node-mongo CLI

[![All Contributors](https://img.shields.io/badge/CLI%20contributors-10-orange)](https://github.com/code-collabo/node-mongo-cli#contributors-) [![npm version](https://badge.fury.io/js/%40code-collabo%2Fnode-mongo-cli.svg)](https://www.npmjs.com/package/@code-collabo/node-mongo-cli) [![Npm package total downloads](https://badgen.net/npm/dt/@code-collabo/node-mongo-cli?color=blue)](https://npmjs.com/package/@code-collabo/node-mongo-cli) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://code-collabo.gitbook.io/node-mongo/contribution-guide/development-mode) [![CLI license: AGPL 3.0](https://img.shields.io/badge/CLI%20licence-AGPL%203.0-blue)](https://github.com/code-collabo/node-mongo-cli/blob/develop/LICENSE) [![API boilerplate templates license: ISC](https://img.shields.io/badge/API%20templates%20licence-ISC-blue)](https://github.com/code-collabo/node-mongo-api-boilerplate-templates/blob/develop/LICENSE) [![GitHub issues](https://img.shields.io/github/issues/code-collabo/node-mongo?color=red)](https://github.com/code-collabo/node-mongo/issues) [![GitHub pull requests](https://img.shields.io/github/issues-pr/code-collabo/node-mongo-cli?color=goldenrod)](https://github.com/code-collabo/node-mongo-cli/pulls)

**Supported node versions:** node v12.x to v18.x

**Operating Systems:** Mac, Windows, and Linux OS

**Parent repo:** [code-collabo/node-mongo](https://github.com/code-collabo/node-mongo)

The [node-mongo-cli](https://www.npmjs.com/package/@code-collabo/node-mongo-cli) is a Command Line Interface made with nodejs. It bootstraps any of the [node-mongo API boilerplate templates](https://github.com/code-collabo/node-mongo-api-boilerplate-templates) for your nodejs mongoDB development, depending on your preference.

### Features

![node-mongo](https://github.com/Ifycode/Ifycode/blob/main/code-collabo/node-mongo-cli.gif?raw=true)

#### CLI

* CLI bootstraps the typescript, es module, or common js (a.k.a. ts, esm, cjs) templates for nodejs mongoDB development.
* Install dependencies and initialize git for the template bootstrapped or choose to skip them.
* Folders are automatically created based on user entry in the prompt or command line.
* The default folder name is used and incremented if the folder name provided already exists.

#### API boilerplate templates

* API boilerplate templates now use the MVC architecture pattern i.e. separated route, model, controller, and service files.
* Development environment already set up with @babel (for esm template only), eslint, and server watch.
* The default connection setup type is MongoDB Atlas. But you get to choose if you want to use it or switch to the Local mongoDB connection setup type.

### CLI installation

Install CLI globally with this command:

```
npm install -g @code-collabo/node-mongo-cli
```

### CLI command

After installing globally, use the node-mongo command.

```
node-mongo
```

### Show CLI help

```
node-mongo --help
```

### CLI usage

```
node-mongo <folder_name> <template>
```

### CLI usage example

Replace \<folder\_name> with your preferred folder name. Replace \<template> with any of these: ts, esm, or cjs. The example below will bootstrap the ts template i.e. the typescript template into a folder named test-folder.

```
node-mongo test-folder ts
```

### CLI flags

```
-h, --help          Show help
-v, --version       Show version number
-i, --install       Install dependencies
-g, --git           Initialize git repo
-s, --skip-install  Skip installing dependencies
-x, --skip-git      Skip initializing git
-y, --yes           See note on --yes flag below
```

### CLI prompts

If you do not specify one or both arguments above, you will be prompted to add your folder name and/or choose template option from list. For foldername, you can choose to use the default foldername provided in the prompt or type in your preferred folder name.

### CLI skip prompts

No prompt when --yes flag is used. It skips both install and git init, and uses esm template as default if no template is specified or if template entered is not in the template collection. In the case of folder name, default foldername is used if no folder name is specified or when folder name already exists.
