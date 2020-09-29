# TubuIO SDK Documentation
## Installation
<!-- tabs:start -->

#### ** Javascript **

npm install @tubuarge/tubuio

### ** Python **
Coming Soon

### ** Java **
Coming Soon


<!-- tabs:end -->

### Usage

Object creation with ApiKey is required to use the SDK.
<!-- tabs:start -->

### ** Javascript **

**Instance Creation**
<br>
Creates an instance to interact with the API
<br>
<br>

**Parameters**
<br>

 1. **ApiKey** (String) - The Api Key of the contract that is obtained from the TUBUIO UI <br>
     

```js
const TubuIO = require('@tubuarge/tubuio')
const tubu = new TubuIO('API_KEY_OF_THE_CONTRACT');

```
**Returns**
<br>
1. Object - The TubuIO object containing Api object.
<br>
<br>
<br>

**TubuIO.createContract(shortID, api)**
<br>
Creates the contract instance to be interacted.
<br>
<br>

**Parameters**
<br>

 1. **ShortID** (String) - The shortID of the contract to be interacted <br>
 2. **Api** (Object) (Optional) - The Api object to interact with the contract of the given shortID, default is the object that is created in TubuIO object declaration 
 <br>

```js
const basicContract = tubu.createContract('CONTRACT_SHORTID', new Api('API_KEY_OF_THE_CONTRACT'));
})
```
**Returns**
<br>
1.Object - The Contract object that can be interacted with call or send methods.
<br>
<br>
<br>

**Contract.call(method, args, tag)**
<br>
Calls the given call method of the contract's given tag version with given args.
<br>
<br>

**Parameters**
1. **method** (String) - The method name in the contract to be called.
2. **args** (Array) (Optional)- The parameters of the method to be called in the contract. If method takes no parameters, the default value is null. Note that methods with parameters will not work without arguments.
3. **tag** (String) (Optional)- The version tag of the contract to be called. If left empty, default contract to be interacted is the latest contract.
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
**Returns**
1. Promise (Object) - A promise object to be resolved.
<br>
<br>
<br>

**Contract.send(method, args, tag)**
<br>
Calls the given send method of the contract's given tag version with given args.
<br>
<br>

**Parameters**
1. **method** (String) - The method name in the contract to be called.
2. **args** (Array) (Optional)- The parameters of the method to be called in the contract. If method takes no parameters, the default value is null. Note that methods with parameters will not work without arguments.
3. **tag** (String) (Optional)- The version tag of the contract to be called. If left empty, default contract to be interacted is the latest contract.
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
**Returns**
1. Promise (Object) - A promise object to be resolved.


### ** Python **
Coming Soon

### ** Java **
Coming Soon

<!-- tabs:end -->

