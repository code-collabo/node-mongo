# API boilerplate templates

[![API boilerplate templates contributors](https://img.shields.io/badge/API%20templates%20contributors-5-orange)](https://github.com/code-collabo/node-mongo-api-boilerplate-templates#contributors-) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://code-collabo.gitbook.io/node-mongo/contribution-guide/development-mode) [![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://github.com/code-collabo/node-mongo-api-boilerplate-templates/blob/develop/LICENSE) [![GitHub issues](https://img.shields.io/github/issues/code-collabo/node-mongo?color=red)](https://github.com/code-collabo/node-mongo/issues) [![GitHub pull requests](https://img.shields.io/github/issues-pr/code-collabo/node-mongo-api-boilerplate-templates?color=goldenrod)](https://github.com/code-collabo/node-mongo-api-boilerplate-templates/pulls)

**Supported node versions:** node v12.x to v18.x

**Parent repo:** [code-collabo/node-mongo](https://github.com/code-collabo/node-mongo)

### Download options

{% tabs %}
{% tab title="Download via CLI" %}
Follow the instructions on the node-mongo CLI npm package to generate your preferred API boilerplate template: [https://www.npmjs.com/package/@code-collabo/node-mongo-cli](https://www.npmjs.com/package/@code-collabo/node-mongo-cli)
{% endtab %}

{% tab title="Manual download option" %}
Find manual download option for the API boilerplate templates at: [https://github.com/code-collabo/node-mongo-api-boilerplate-templates](https://github.com/code-collabo/node-mongo-api-boilerplate-templates)
{% endtab %}
{% endtabs %}

### Connection options or setup type

{% tabs %}
{% tab title="MongoDB Atlas" %}
**Step 1**

Install dependencies:

```
npm install
```

**Step 2**

* Have a mongoDB atlas cluster set up in the cloud
* Get your atlas mongoDB uri string

**Step 3**

* Rename the `.env.example` file to `.env`
* Change `PORT` environment variable from `8080` to preferred port number in the .env file
* Add your atlas mongoDB uri string to the `MONGODB_ATLAS_URI` environment variable in the .env file

**Step 4**

Start dev server for connection to mongoDB atlas:

```
npm run dev:atlas
```
{% endtab %}

{% tab title="Local MongoDB" %}
**Step 1**

Install dependencies:

```
npm install
```

**Step 2**

* Have mongoDB installed and running on your computer
* Get your local mongoDB uri string

**Step 3**

* Rename the `.env.example` file to `.env`
* Change `PORT` environment variable from `8080` to preferred port number in the .env file
* Add your local mongoDB uri string to the `MONGODB_LOCAL_URI` environment variable in the .env file

**Step 4**

Start dev server for connection to local mongoDB:

```
npm run dev:local
```
{% endtab %}
{% endtabs %}

