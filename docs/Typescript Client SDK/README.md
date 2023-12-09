---
title: Typescript Client SDK
---
# Typescript Client SDK

### Overview

To make Identigo easy to use, we've created a nice and simple SDK.
You'll import the SDK in to your frontend projects and it will handle authentication with your Identigo server for you.

### Installation

Add the package to your project

```bash
npm i @designlogica/identigo-client-sdk
```

You need to import the library and initialise it, this should be done at the earliest possible time.

```typescript
import {Identigo} from '@designlogica/Identigo';

const url = 'localhost:3000'; // your Identigo Server Url.
const appId = 'yourAppId';
const auth = new Identigo(url, appId);

async function init(){
    await auth.init();
}

init();

```

Doing this at the earliest possible time is important because part of the initialisation is also checking to see if we are already logged in, or if we are about to exchange tokens with the server.



