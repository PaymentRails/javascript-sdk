
# Payment Rails JavaScript SDK

A JavaScript SDK (written in TypeScript) - For more information about the API as well as NodeJS code samples check out the [full API documentation](http://docs.paymentrails.com)


## Installation

    npm install --save paymentrails

## Getting Started

```js
// A simple application using the Payment Rails SDK
const PaymentRails = require('paymentrails');

PaymentRails.Configuration.setApiKey("YOUR-API-KEY");
PaymentRails.Configuration.setApiSecret("YOUR-API-SECRET");
PaymentRails.Configuration.setEnviroment("production");

async function main() {
    const recipient = await PaymentRails.Recipient.find("R-G7SXXpm6cs4aTUd9YhmgWC");
    console.log(recipient.id);
}

main();
```

### Usage

Methods should all have JSDoc comments to help you understand their usage. As mentioned the [full API documentation](http://docs.paymentrails.com)
is the best source of information about the API.

For more information please read the [JavaScript API docs](https://github.com/PaymentRails/javascript-sdk/blob/master/docs/api.md) is available.

#### Running Unit tests

If you're working on the library itself, here's easy way to run the unit tests. They are designed to be run with configuration coming through environment variables.
  
  * ``PR_ACCESS_KEY``
  * ``PR_SECRET_KEY``
  * ``PR_ENVIRONMENT``

For a command like:
    
    PR_ACCESS_KEY=xxx \
    PR_SECRET_KEY=yyy \
    PR_ENVIRONMENT=integration \
    npm run test:integration




## Index

### External modules

* ["Balance"](modules/_balance_.md)
* ["BalanceGateway"](modules/_balancegateway_.md)
* ["Batch"](modules/_batch_.md)
* ["BatchGateway"](modules/_batchgateway_.md)
* ["Client"](modules/_client_.md)
* ["Configuration"](modules/_configuration_.md)
* ["Gateway"](modules/_gateway_.md)
* ["Payment"](modules/_payment_.md)
* ["PaymentGateway"](modules/_paymentgateway_.md)
* ["Recipient"](modules/_recipient_.md)
* ["RecipientAccount"](modules/_recipientaccount_.md)
* ["RecipientAccountGateway"](modules/_recipientaccountgateway_.md)
* ["RecipientGateway"](modules/_recipientgateway_.md)
* ["exceptions/index"](modules/_exceptions_index_.md)
* ["index"](modules/_index_.md)
* ["types"](modules/_types_.md)



---