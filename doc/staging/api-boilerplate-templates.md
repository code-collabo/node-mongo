# API boilerplate templates

[![API boilerplate templates contributors](https://img.shields.io/badge/API%20templates%20contributors-5-orange)](https://github.com/code-collabo/node-mongo-api-boilerplate-templates#contributors-) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://code-collabo.gitbook.io/node-mongo-v2.0.0/contribution-guide/node-mongo) [![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://github.com/code-collabo/node-mongo-api-boilerplate-templates/blob/develop/LICENSE) [![GitHub issues](https://img.shields.io/github/issues/code-collabo/node-mongo?color=red)](https://github.com/code-collabo/node-mongo/issues) [![GitHub pull requests](https://img.shields.io/github/issues-pr/code-collabo/node-mongo-api-boilerplate-templates?color=goldenrod)](https://github.com/code-collabo/node-mongo-api-boilerplate-templates/pulls)

{% hint style="info" %}
node-mongo projects require you to have Node.js or Node Version Manager (NVM) installed on your computer
{% endhint %}

**Parent repo:** [code-collabo/node-mongo](https://github.com/code-collabo/node-mongo)

{% hint style="info" %}
API boilerplate templates v1.0.0
{% endhint %}

### Features

* Three (3) API boilerplate templates to choose from i.e. typescript, es module, or common js templates (a.k.a. ts, esm, cjs) for your nodejs mongoDB development, depending on your preference.
* API boilerplate templates now use the MVC architecture pattern i.e. separated route, model, controller, and service files.
* Development environment already set up with @babel (for esm template only), eslint, and server watch.
* The default connection setup type is MongoDB Atlas. You get to choose if you want to use Atlas or switch to the Local mongoDB connection setup type, and you also get to save your preferred connection type for when next you run the automated dev server.
* Improved user experience with the newly added walk-through prompts in the terminal: quick to setup, easy to use, with automated and improved user support.

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
````
npm install
````

**Step 2**
- Ensure you have internet connection
- Have a monogDB atlas cluster set up in the cloud
- Get your atlas mongoDB uri string

**Step 3**
- Rename the `.env.example` file to `.env`
- Change `PORT_ATLAS` environment variable to your preferred port number in the .env file
- Add your atlas mongoDB uri string to the `MONGODB_ATLAS_URI` environment variable in the .env file

**Step 4**
Start the automated dev server and choose ATLAS connection:
````
npm run dev
````

**Step 4 (alternative)**
You can also use the (manual) dev server alternative for connection to mongoDB atlas:
````
npm run dev:atlas
````
{% endtab %}

{% tab title="Local MongoDB" %}

**Step 1**

Install dependencies:
````
npm install
````

**Step 2**
- Have mongoDB installed and running on your computer
- Get your local mongoDB uri string

**Step 3**
- Rename the `.env.example` file to `.env`
- Change `PORT_LOCAL` environment variable to your preferred port number in the .env file
- Add your local mongoDB uri string to the `MONGODB_LOCAL_URI` environment variable in the .env file

**Step 4**
Start the automated dev server and choose LOCAL connection:
````
npm run dev
````

**Step 4 (alternative)**
You can also use the (manual) dev server alternative for connection to local mongoDB:
````
npm run dev:local
````
{% endtab %}
{% endtabs %}

### Automated node-mongo-scripts

- `npm run dev` prompts you to choose your preferred connection setup type the first time you use it, and saves the chosen connection type for every other time you come back to use it. It also automatically installs or set up the db and server files for the chosen connection set up type.
- `npm run dev:restore` resets the application back to first time usage condition (i.e. it removes your previously saved connection setup type). After using this command, you will now have the option to set your preferred connection type again the next time you start the server with the `npm run dev` command.
- `npm run change:connection` is useful for when you are not a first time user and want to change your connection set up type without restoring the application to first time usage condition. It will prompt you to choose your connection type, but it will not install the db and server files for the chosen connection set up type.

### Testing with the demo setup
A demo setup (i.e. collection, endpoints etc) already exists to help you get started with using the node-mongo API boilerplate templates. Running the demo setup will help you understand how to create your own collection endpoints etc. The API design and API call requests and responses sections below will help you understand how the demo setup works.

### API design

|METHOD /endpoint|Description|Request body|
|--|--|:--:|
|GET /demo|Get all demo items in the database| No Request Body |
|POST /demo|Create/add new demo item to the database|name, age|
|GET /demo/:demoId|Get a demo item stored in the database by its ID|No Request Body|
|PATCH /demo/:demoId|Update the value of one property of an already existing demo item in the database, using the demo item's ID|propName, value|
|PUT /demo/:id|Update all properties of an existing demo item in the database, using the demo item's ID|name, age|
|DELETE /demo/:demoId|Delete a demo item from the database, using the demo item's ID|No request body|

### API call requests and responses

<details>
<summary>GET /demo</summary>
<br/>
    <b>Request body (sample format)</b>
    <br/><br/>
<pre>
No request body
</pre>
<br/>
     <b>Successful response (sample format)</b>
    <br/><br/>
<pre>
{
    "count": number,
    "items": [
        {
            "_id": "string",
            "name": "string",
            "age": number,
            "request": {
                "type": "string",
                "url": "string"
            }
        },
        // etc.
    ]
}
</pre>
</details>



<details>
<summary>POST /demo</summary>
<br/>
    <b>Request body (sample format)</b>
    <br/><br/>
<pre>
{
    "name": "string",
    "age": number
}
</pre>
<br/>
     <b>Successful response (sample format)</b>
    <br/><br/>
<pre>
{
    "message": "string",
    "newItem": {
        "_id": "string",
        "name": "string",
        "age": number,
        "request": {
            "type": "string",
            "url": "string"
        }
    }
}
</pre>
</details>



<details>
<summary>GET /demo/:demoId</summary>
<br/>
    <b>Request body (sample format)</b>
    <br/><br/>
<pre>
No request body
</pre>
<br/>
     <b>Successful response (sample format)</b>
    <br/><br/>
<pre>
{
    "_id": "string",
    "name": "string",
    "age": number,
    "request": {
        "type": "string",
        "description": "string",
        "url": "string"
    }
}
</pre>
</details>



<details>
<summary>PATCH /demo/:demoId</summary>
<br/>
    <b>Request body (sample format)</b>
    <br/><br/>
<pre>
[
    { "propName": "string", "value": "string" or number }
]
</pre>
i.e. propName can be string "name" or "age". Value is a string when name is the propName, while value is a number when age is the propName.
<br/>
<br/>
     <b>Successful response (sample format)</b>
    <br/><br/>
<pre>
{
    "message": "string",
    "request": {
        "type": "string",
        "description": "string",
        "url": "string"
    }
}
</pre>
</details>



<details>
<summary>PUT /demo/:id</summary>
<br/>
    <b>Request body (sample format)</b>
    <br/><br/>
<pre>
{
    "name": "string",
    "age": number
}
</pre>
<br/>
     <b>Successful response (sample format)</b>
    <br/><br/>
<pre>
{
    "message": "string",
    "request": {
        "type": "string",
        "description": "string",
        "url": "string"
    }
}
</pre>
</details>



<details>
<summary>DELETE /demo/:demoId</summary>
<br/>
    <b>Request body (sample format)</b>
    <br/><br/>
<pre>
No request body
</pre>
<br/>
     <b>Successful response (sample format)</b>
    <br/><br/>
<pre>
{
    "message": "string",
    "request": {
        "type": "string",
        "description": "string",
        "url": "string",
        "body": {
            "name": "string",
            "age": "string"
        }
    }
}
</pre>
</details>

