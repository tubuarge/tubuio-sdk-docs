# NodeJS SDK

## Create Instance

```js
const Tubu = require('@tubu/tubuio-sdk-node');
const app = new Tubu('APP_API_KEY');
```

#### Parameters

- **ApiKey** (`String`) - The Api Key of the contract that is obtained from [app.tubu.io](https://app.tubu.io)

## Contract

```js
const contract = app.contract('CONTRACT_SHORTID');
```

#### Parameters

- **ShortID** (`String`) - The shortID of the contract to be interacted


### call

> **contract.call(method, args, tag)**

Calls the given call method of the contract's given tag version with given args.

#### Parameters

- **method** (`String`) - The method name in the contract to be called.
- **args** (`Array`) (*Optional*)- The parameters of the method to be called in the contract. If method takes no parameters, the default value is null. Note that methods with parameters will not work without arguments.
- **tag** (`String`) (*Optional*)- The version tag of the contract to be called. If left empty, default contract to be interacted is the latest contract.

```js
contract
    .call('METHOD_NAME', args = [])
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
> **contract.send(method, data, tag)**

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
contract
    .send('METHOD_NAME', { args: [], account: 'ACCOUNT_ADDRESS' })
    .then((result) => {
        console.log(result.data);
    })
    .catch((err) => {
        console.log(err);
    });
```

#### Returns
- Promise (`Object`) - A promise object to be resolved.