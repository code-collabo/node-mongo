---
description: NODE-MONGO CONTRIBUTOR DOCUMENTATION
---

# ℹ Contributors guide: node-mongo setup and development


### Contributor's individual project development guide

{% tabs %}
{% tab title="CLI" %}

Contributors are to run the CLI commands and flags as described on the CLI repo readme: [https://github.com/code-collabo/node-mongo-cli](https://github.com/code-collabo/node-mongo-cli)

The method of installation is different during code development:

1. Install Dependencies:

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
### Learning Resources
- [Twilo | Dominik Kundel: How to build a CLI with node.js](https://youtu.be/s2h28p4s-Xs) - Youtube Video
- [Twilo | Dominik Kundel: How to build a CLI with node.js](https://www.twilio.com/blog/how-to-build-a-cli-with-node-js) - Blog Post

{% endtab %}
{% tab title="API Boilerplate Templates" %}

Contributors are to run the project as described on the API boilerplate templates repo readme: [https://github.com/code-collabo/node-mongo-api-boilerplate-templates](https://github.com/code-collabo/node-mongo-api-boilerplate-templates)

How to handle the `.env` files is different during code development:

- Retain the `.env.example` file so that it doesn't get deleted from our repo when you are submitting your code fix

- Create a copy of the `.env.example` file, rename this copy to `.env` , then change the `PORT` and add other environment variables to store your secrets as desired.

### Learning Resources
- [TomDoesTech: REST API with Node.js, Express, typescript, MongoDB $ Zod.](https://youtu.be/s2h28p4s-Xs)
- [TomDoesTech: Module "mongoose" has no exported member 'DocumentDefinition'.ts (tutorial fixes).](https://youtu.be/s2h28p4s-Xs)
- [Academind: Building a RESTFUL API with node.js](https://youtu.be/s2h28p4s-Xs)
- [CodeAffection: MEAN stack CRUD operations](https://youtu.be/s2h28p4s-Xs) - first 33 minutes

{% endtab %}
{% endtabs %}