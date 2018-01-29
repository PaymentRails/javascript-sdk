# Payment Rails JavaScript SDK

A JavaScript SDK (written in TypeScript) - For more information about the API as well as NodeJS code samples check out the [full API documentation](http://docs.paymentrails.com)


## Installation

    npm install --save paymentrails

## Getting Started

The Payment Rails API is built using promises and all methods except
connect will return a promise. The connect call allows you to setup
your API Key and Secret with a client that can be used for subsequent
calls.

```js
// A simple application using the Payment Rails SDK
const paymentrails = require('paymentrails');

const client = paymentrails.connect({
  key: "YOUR-API-KEY",
  secret: "YOUR-API-SECRET",
  environment: "production",
});

// Async/Await version

async function main() {
  const recipient = await client.recipient.find("R-G7SXXpm6cs4aTUd9YhmgWC");
  console.log(recipient.id);
}

main();

// Promise version

client.recipient.find("R-G7SXXpm6cs4aTUd9YhmgWC").then(recipient => {
  console.log(recipient.id);
}).catch(err => {
  console.log("ERROR", err);
});

```

### Usage

Methods should all have JSDoc comments to help you understand their usage. As mentioned the [full API documentation](http://docs.paymentrails.com)
is the best source of information about the API.

For more information please read the [JavaScript API docs](https://github.com/PaymentRails/javascript-sdk/blob/master/docs/api.md) is available.

#### Running Integration / Unit tests

If you're working on the library itself, here's easy way to run the unit tests. They are designed to be run with configuration coming through environment variables.

  * ``PR_ACCESS_KEY``
  * ``PR_SECRET_KEY``
  * ``PR_ENVIRONMENT``

For a command like:
    
    PR_ACCESS_KEY=xxx \
    PR_SECRET_KEY=yyy \
    PR_ENVIRONMENT=integration \
    npm run test:integration

