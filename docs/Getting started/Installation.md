---
title: 02. Installation
---
# Installation

To get started, first clone the repo.
```bash
git clone git@github.com:designLogica/identigo-server.git
```

cd into the folder and install

```bash
npm i
```

Setup your .env file with the following entries

```
APP_SECRET=ALongSecretString
REFRESH_TOKEN_SECRET=AnotherLongString
MONGO_URI=mongodb://yourMongoConnectionString
```
Then you can run the server with
```bash
npm start
```

You can check the home page at <a href="http://localhost:3000">localhost:3000</a>

And view the admin panel <a href="http://localhost:3000/admin">localhost:3000/admin</a>