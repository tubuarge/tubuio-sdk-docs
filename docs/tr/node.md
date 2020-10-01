# NodeJS SDK

## Create Instance

```js
const Tubu = require('@tubuarge/Tubu')
const tubuApp = new Tubu('API_KEY_OF_AN_APPLICATION');
```

#### Parameters

- **ApiKey** (`String`) - The Api Key of the contract that is obtained from [app.tubu.io](https://app.tubu.io)

## Contract

```js
const basicContract = tubu.createContract('CONTRACT_SHORTID');
```

#### Parameters

- **ShortID** (`String`) - The shortID of the contract to be interacted


### call

> **basicContract.call(method, args, tag)**

Calls the given call method of the contract's given tag version with given args.

#### Parameters

- **method** (`String`) - The method name in the contract to be called.
- **args** (`Array`) (*Optional*)- The parameters of the method to be called in the contract. If method takes no parameters, the default value is null. Note that methods with parameters will not work without arguments.
- **tag** (`String`) (*Optional*)- The version tag of the contract to be called. If left empty, default contract to be interacted is the latest contract.

```js
basicContract
    .send('addItem', { args: ['xyz', 13, false] })
    .then((result) => {
        console.log(result.data);
    })
    .catch((err) => {
        console.log(err);
    });
```

#### Returns
- Promise (`Object`) - A promise object to be resolved.

### send
> **basicContract.send(method, data, tag)**

Calls the given send method of the contract's given tag version with given args.

#### Parameters
- **method** (`String`) - The method name in the contract to be called.
- **data** (`Object`) (*Optional*) - The parameters of the method to be called in the contract. If method takes no parameters, the default value is null. Note that methods with parameters will not work without arguments.
```js
// data
{
    "args": [], // An array of arguments of the method (Optional)
    "account": "string" // Sender account address (Optional)
}
```
- **tag** (`String`) (*Optional*)- The version tag of the contract to be called. If left empty, default contract to be interacted is the latest contract.

```js
basicContract
    .send('addItem', { args: ['xyz', 13, false], account: 'SENDER_ACCOUNT_ADDRESS' }, 'v1.1')
    .then((result) => {
        console.log(result.data);
    })
    .catch((err) => {
        console.log(err);
    });
```

#### Returns
- Promise (`Object`) - A promise object to be resolved.