---
description: NODE-MONGO FEATURES AND COMMANDS DOCUMENTATION
---

# ℹ Reference Guide: node-mongo features and commands

***

_On this documentation page, you will find more details on node-mongo's features and commands, and the various types of API boilerplate templates you can generate._

***

## Features

![node-mongo gif tutorial](https://github.com/Ifycode/Ifycode/blob/main/code-collabo/node-mongo-cli.gif?raw=true)

### CLI features

* CLI bootstraps the API boilerplate templates for nodejs mongoDB development.
* Install dependencies and initialize git for the template bootstrapped or choose to skip them.
* Folders are automatically created based on user entry in the prompt or command line.
* The default folder name is used and incremented if the folder name provided already exists.

### API boilerplate template features

* Three (3) API boilerplate templates to choose from i.e. typescript, es module, or common js templates (a.k.a. ts, esm, cjs) for your nodejs mongoDB development, depending on your preference.
* API boilerplate templates now use the MVC architecture pattern i.e. separated route, model, controller, and service files.
* Development environment already set up with @babel (for esm template only), eslint, and server watch.
* The default connection setup type is MongoDB Atlas. You get to choose if you want to use Atlas or switch to the Local mongoDB connection setup type, and you also get to save your preferred connection setup type for when next you run the automated development server.
* Improved user experience with the newly added walk-through prompts in the terminal: quick to setup, easy to use, with automated and improved user support.

***

### CLI command

After installing globally once (as shown in the quick guide), use the node-mongo command any time you want node-mongo to execute:

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

Replace \<folder\_name> with your preferred folder name. Replace \<template> with any of these: ts, esm, or cjs. The example below will bootstrap the esm template i.e. the ES module template into a folder named new-test-folder.

```
node-mongo new-test-folder esm
```

### CLI flags

```
-h, --help          Show help
-v, --version       Show version number
-i, --install       Install dependencies
-g, --git           Initialize git repo
-s, --skip-install  Skip installing dependencies
-x, --skip-git      Skip initializing git
-y, --yes           No prompt: See note on --yes flag below
```

### CLI prompts

If you do not specify one or both (foldername or template) arguments as shown above, you will be prompted to add your folder name and/or choose template option from list. For foldername, you can choose to use the default foldername provided in the prompt or type in your preferred folder name.

### CLI skip prompts

No prompt when --yes flag is used. It skips both install and git init. The CLI will generate the (default) ts template if no template is specified or if the template entered is not in the template collection. In the case of folder name, default foldername is used if no folder name is specified or when the folder name used already exists.
