---
description: NODE-MONGO USER DOCUMENTATION
---

# ℹ User guide: node-mongo setup, installation and usage

***

Build backend applications for your projects with node-mongo. _This is a quick setup, installation, and usage guide. On this page, you will learn how to quickly create a new backend API using node-mongo. Follow hints that give instructions on where to find more robust content on the node-mongo features and commands, or you can just simply check the sidebar._

***

{% hint style="info" %}
* _**Operating System Requirements:**_ Works on Mac, Windows, and Linux Operating Systems.
* _**Installation Requirements:**_ To be able to use node-mongo, you need Node js to be installed on your computer. You can get Node js from the official Node js website, or install Node js through the Node Version Manager (NVM).
* _**Supported Node.js versions:**_ Node js versions 16.x - 20.x
{% endhint %}

![node-mongo gif tutorial](https://github.com/Ifycode/Ifycode/blob/main/code-collabo/node-mongo-cli.gif?raw=true)

***

## Install node-mongo CLI

Install CLI globally using this command:

```
npm install -g @code-collabo/node-mongo-cli
```

## Create a new backend API application

Change directory i.e. cd into any folder of choice on your computer. Then run the `node-mongo` command together with `test-folder` and `ts` as shown in the code block below. This will generate a new backend API called test-folder, and the code in the application generated will be in typescript (ts).

```
node-mongo test-folder ts
```

***

{% hint style="info" %}
See _**Reference Guide: node-mongo features and commands**_ for more details on other types of templates you can generate apart from the typescript (ts) template. You can find this in the sidebar.
{% endhint %}

***

## Running the generated backend API application

Change directory i.e. cd into the `test-folder` application generated earlier. Then follow the steps below depending on the MongoDB connection or setup type that you wish to use.

{% tabs %}
{% tab title="MongoDB Atlas" %}
**Step 1**

Install dependencies:

```
npm install
```

**Step 2**

* Ensure you have an internet connection
* Have a monogDB atlas cluster set up in the cloud
* Get your Atlas mongoDB URI string

**Step 3**

* Rename the `.env.example` file to `.env`
* Change `PORT_ATLAS` environment variable to your preferred port number in the .env file
* Add your Atlas mongoDB URI string to the `MONGODB_ATLAS_URI` environment variable in the .env file

**Step 4**

Start the automated development server and choose ATLAS connection:

```
npm run dev
```

**Step 4 (alternative)**

You can also use the (manual) development server alternative for connection to MongoDB atlas:

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

* Have MongoDB installed and running on your computer
* Get your local MongoDB URI string

**Step 3**

* Rename the `.env.example` file to `.env`
* Change `PORT_LOCAL` environment variable to your preferred port number in the .env file
* Add your local MongoDB URI string to the `MONGODB_LOCAL_URI` environment variable in the .env file

**Step 4**

Start the automated development server and choose LOCAL connection:

```
npm run dev
```

**Step 4 (alternative)**

You can also use the (manual) development server alternative for connection to local MongoDB:

```
npm run dev:local
```
{% endtab %}
{% endtabs %}

***

`npm run dev` starts the automated development server. It prompts you to choose your preferred connection setup type the first time you use it and saves the chosen connection setup type for every other time you come back to use it. It also automatically installs or sets up the DB and server files for the chosen connection setup type.

`npm run dev:restore` resets the automated development server back to first-time usage condition i.e. it removes your previously saved connection setup type and the development server will now assume that you are a first-timer. After using this command, you will now have the option to set your preferred connection type again the next time you start the server with the `npm run dev` command.

`npm run dev:change` is useful for when you are not a first-time user and want to change your connection setup type without restoring the automated development server to first-time usage condition. It will prompt you to choose your connection setup type, but it will not install the DB and server files for the chosen connection setup type.

***

## API design

A "demo" setup exists in the generated backend API application i.e. `demo` database collection and schema, `/demo` endpoints, etc. that you can test with. Find more details about the available test endpoints that you can try out in the table below:

<table><thead><tr><th width="252.33333333333331">METHOD /endpoint</th><th>Description</th><th align="center">Request body</th></tr></thead><tbody><tr><td>GET /demo</td><td>Get all demo items in the database</td><td align="center">No Request Body</td></tr><tr><td>POST /demo</td><td>Create/add new demo item to the database</td><td align="center">name, age</td></tr><tr><td>GET /demo/:demoId</td><td>Get a demo item stored in the database by its ID</td><td align="center">No Request Body</td></tr><tr><td>PATCH /demo/:demoId</td><td>Update the value of one property of an already existing demo item in the database, using the demo item's ID</td><td align="center">propName, value</td></tr><tr><td>PUT /demo/:id</td><td>Update all properties of an existing demo item in the database, using the demo item's ID</td><td align="center">name, age</td></tr><tr><td>DELETE /demo/:demoId</td><td>Delete a demo item from the database, using the demo item's ID</td><td align="center">No request body</td></tr></tbody></table>

{% hint style="info" %}
_**Volunteer:**_ Contribute to this doc. Help users know how they can add their own db collections, schemas, endpoints, files, etc. to the generated backend API application.
{% endhint %}

***

## API call requests and responses

<details>

<summary>GET /demo</summary>

Request body shape

```
No request body
```

Successful response shape

```
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
```

</details>

<details>

<summary>POST /demo</summary>

Request body shape

```
{
    "name": "string",
    "age": number
}
```

Successful response shape

```
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
```

</details>

<details>

<summary>GET /demo/:demoId</summary>

Request body shape

```
No request body
```

Successful response shape

```
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
```

</details>

<details>

<summary>PATCH /demo/:demoId</summary>

Request body shape

```
[
    { "propName": "string", "value": "string" }
]

OR

[
    { "propName": "string", "value": number }
]
```

i.e. propName can be string "name" or "age". Value is a string when name is the propName, while value is a number when age is the propName.

Successful response shape

```
{
    "message": "string",
    "request": {
        "type": "string",
        "description": "string",
        "url": "string"
    }
}
```

</details>

<details>

<summary>PUT /demo/:id</summary>

Request body shape

```
{
    "name": "string",
    "age": number
}
```

Successful response shape

```
{
    "message": "string",
    "request": {
        "type": "string",
        "description": "string",
        "url": "string"
    }
}
```

</details>

<details>

<summary>DELETE /demo/:demoId</summary>

Request body shape

```
No request body
```

Successful response shape

```
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
```

</details>

{% hint style="info" %}
_**Volunteer:**_ Contribute to this doc and node-mongo API. Help create swagger documentation for testing API call requests and responses, and help link to this doc. Instead of what we have here now.
{% endhint %}
