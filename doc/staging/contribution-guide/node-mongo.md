# Node mongo contribution guide

{% hint style="info" %}
Start from the [Collabo community contribution guide](https://code-collabo.gitbook.io/community-doc/collabo-guidelines/contributing) 👋
{% endhint %}

### Contributor's individual project development guide

{% tabs %}
{% tab title="CLI" %}
Contributors are to run the CLI commands and flags as described on the CLI repo readme: [https://github.com/code-collabo/node-mongo-cli](https://github.com/code-collabo/node-mongo-cli)

The method of installation is different during code development:

1. Install dependencies

```
npm install
```

2. Link after installing dependencies:

```
npm link
```

3. Unlink (for when you are done developing):

```
npm unlink
```

#### Learning resources

* [Twilio | Dominik Kundel: How to build a CLI with node.js](https://youtu.be/s2h28p4s-Xs) - _youTube video_.
* [Twilio | Dominik Kundel: How to build a CLI with node.js](https://www.twilio.com/blog/how-to-build-a-cli-with-node-js) _- blog post._
{% endtab %}

{% tab title="API boilerplate templates" %}
Contributors are to run the project as described on the API boilerplate templates repo readme: [https://github.com/code-collabo/node-mongo-api-boilerplate-templates](https://github.com/code-collabo/node-mongo-api-boilerplate-templates)

How to handle the `.env` files is different during code development:

* Retain the `.env.example` file so that it doesn't get deleted from our repo when you are submitting your code fix
* Create a copy of the `.env.example` file, rename this copy to `.env` , then change the `PORT` and add other environment variables to store your secrets as desired.

#### Learning resources

* [TomDoesTech: REST API with Node.js, Express, TypeScript, MongoDB & Zod](https://www.youtube.com/watch?v=BWUi6BS9T5Y).
* [TomDoesTech: Module '"mongoose"' has no exported member 'DocumentDefinition'.ts (tutorial fixes)](https://www.youtube.com/watch?v=5-1KuU-21uI).
* [Academind: Building a restful API with node.js](https://academind.com/tutorials/building-a-restful-api-with-nodejs/).
* [CodAffection: MEAN stack CRUD operations](https://youtu.be/UYh6EvpQquw) - _1st 33 minutes_.
{% endtab %}
{% endtabs %}

