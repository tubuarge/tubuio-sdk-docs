# tubuio-sdk-docs
documentation for tubuio sdk
## Installation
<!-- tabs:start -->

#### ** Javascript **

npm install @tubuarge/tubuio

#### ** Python **

pip install tubuio


<!-- tabs:end -->

## Usage

Instance creation and user login is required to use the modules of the SDK
<!-- tabs:start -->

### ** Javascript **

<strong>Instance Creation </strong>
<br>
Creates an instance to interact with the API
<br>
<br>
<strong>Parameters</strong>
<br>
 1. Object <br>
    - urlbase-String: The URL of the API 

```js
const TubuIO = require('@tubuarge/tubuio')
const instance = new TubuIO({
    urlbase: 'https://api-test.tubu.io'
})
```

<strong> TubuIO.login(credentials) </strong>
<br>
Logs in to the API using the username and password
<br>
<br>
<strong>Parameters</strong>
<br>
 1. Object - User credentials for logging in <br>

```js
TubuIO.login({
    username: 'user1',
    password: 'password1'
})
```

### ** Python **

<strong>Instance Creation </strong>
<br>
Creates an instance to interact with the API
<br>
<br>
<strong>Parameters</strong>
<br>
 1. Dictionary <br>
    - urlbase-String: The URL of the API 

```python
tubuio_user =  new TubuIO({
    urlbase: 'https://api-test.tubu.io'
})
```

<strong> (TubuIO)Object.login(credentials) </strong>
<br>
Logs in to the API using the username and password
<br>
<br>
<strong>Parameters</strong>
<br>
 1. dict - User credentials stored in dictionary for logging in <br>

```js
tubuio_user.login({
    username: 'user1',
    password: 'password1'
})
```



<!-- tabs:end -->

## Modules

### Network
<!-- tabs:start -->

### ** Javascript **
<strong> network.getAll(options)</strong>
<br>
Fetches all the networks of the current user
<br>
<br>
<strong>Parameters</strong>
<br>
 1. Object -(optional) Query options<br>


```js

TubuIO.network.getAll({
    page: 1,
    pageSize: 100
})

```
<br>
<br>
<strong> network.getByID(networkID)</strong>
<br>
Fetches the network of the user with the given ID 
<br>
<br>
<strong>Parameters</strong>
<br>
 1. Number - The ID of the Network that is going to be fetched <br>

```js

TubuIO.network.getByID(14)

```
### ** Python **

<strong> network.getAll(options)</strong>
<br>
Fetches all the networks of the current user
<br>
<br>
<strong>Parameters</strong>
<br>
 1. dict -(optional) Query options<br>


```python

TubuIO.network.getAll({
    page: 1,
    pageSize: 100
})

```
<br>
<br>
<strong> network.getByID(networkID)</strong>
<br>
Fetches the network of the user with the given ID 
<br>
<br>
<strong>Parameters</strong>
<br>
 1. int - The ID of the Network that is going to be fetched <br>

```python

TubuIO.network.getByID(14)

```


<!-- tabs:end -->
### Application
<!-- tabs:start -->

### ** Javascript **
<strong> application.createApp(networkID, appDetails)</strong>
<br>
Creates an application in the network with given networkID using the appDetails
<br>
<br>
<strong>Parameters</strong>
<br>
 1. Number - The ID of the Network that app is going to be created in <br>
 2. Object - The name and description of the app that is going to be created <br>

```js

TubuIO.application.createApp(8, {
    name: "Sample App"
    description: "Description of the Sample App"
})
```
### ** Python **

<strong> application.createApp(networkID, appDetails)</strong>
<br>
Creates an application in the network with given networkID using the appDetails
<br>
<br>
<strong>Parameters</strong>
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. dict - The name and description of the app that is going to be created <br>

```python

TubuIO.application.createApp(8, {
    name: "Sample App"
    description: "Description of the Sample App"
})
```
<br>
<strong> application.getApps(networkID, appDetails)</strong>
<br>
The method to get the current user's applications on the specific network.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. dict - The name and description of the app that is going to be created <br>

```python

TubuIO.application.getApps(8, {
    name: "Sample App"
    description: "Description of the Sample App"
})
```

<br>
<strong> application.getApp(networkID, appID)</strong>
<br>
The method to get the current user's specific application on the specific network using the networkID and appID.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. int - The ID of the Application that is to be queried <br>

```python

TubuIO.application.getApp(8, 6)
```

<br>
<strong> application.updateApp(networkID, appID, updateDetails)</strong>
<br>
The method to update the current user's specific application on the specific network using the networkID and appID.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. int - The ID of the Application that is to be queried <br>
 3. dict - The new name and description of the app that is going to be updated <br>

```python

TubuIO.application.updateApp(8, 6, {
    name: "Sample App"
    description: "Description of the Sample App"
})
```

<br>
<strong> application.deleteApp(networkID, appID)</strong>
<br>
The method to get the current user's specific application on the specific network using the networkID and appID.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. int - The ID of the Application that is to be queried <br>

```python

TubuIO.application.deleteApp(8, 6)
```

<!-- tabs:end -->
### Contract
<!-- tabs:start -->

### ** Javascript **

```js
const TubuIO = require('@tubuarge/tubuio')
const instance = new TubuIO({
    urlbase: 'https://api-test.tubu.io'
})

instance.login({
    username: 'user1',
    password: 'password1'
})
```
### ** Python **

<strong> contract.deploy(networkID, contractDetails)</strong>
<br>
Deploys a contract in the network with given networkID using the contractDetails
<br>
<br>
<strong>Parameters</strong>
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. dict - The name, description and application id of the contract that is going to be deployed <br>

```python

TubuIO.contract.deploy(8, {
    name: "Sample App"
    description: "Description of the Sample App"
    appID: "8"
})
```
<br>
<br>
<strong> contract.getAll(networkID, pageDetails)</strong>
<br>
The method to get the current user's contracts on the specific network.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. dict - The page, page size and application id of the contract that is going to be obtained <br>

```python

TubuIO.contract.getAll(8, {
    page: "1"
    page_size: "100"
    app_id: "8"
})
```

<br>
<br>
<strong> contract.getByShortId(contractDetails)</strong>
<br>
The method to get the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. dict - The network id and the short contract id of the contract that is going to be obtained <br>

```python

TubuIO.contract.getByShortId({
    networkID: "2"
    shortID: "sad1231"
})
```

<br>
<br>
<strong> contract.delete(contractDetails)</strong>
<br>
The method to get the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. dict - The network id and the short contract id of the contract that is going to be deleted <br>

```python

TubuIO.contract.delete({
    networkID: "2"
    shortID: "sad1231"
})
```

<br>
<br>
<strong> contract.update(networkDetails, contractDetails)</strong>
<br>
The method to update the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. dict - The ID of the Network and the short ID of the contract that is going to be updated in <br>
 2. dict - The name and description of the contract <br>

```python
TubuIO.contract.update({
    networkID: "2"
    shortID: "sad1231"
}, {
    name: "Sample Name"
    description: "Sample Description"
})
```

<br>
<br>
<strong> contract.invoke(contractDetails, args)</strong>
<br>
The method to invoke the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. dict - The short ID of the contract and the method that is going to be invoked in <br>
 2. dict - The args of the method <br>

```python
TubuIO.contract.invoke({
    shortID: "sad1231"
    method: "getCount"
}, {
    args: ["300", "200", "0X1231312asdsadad"]
})
```

<br>
<br>
<strong> contract.call(networkDetails, contractDetails)</strong>
The method to call the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>
<strong>Parameters</strong>
<br>
1. dict - The short ID of the contract and the method that is going to be called in <br>
2. dict - The args of the method <br>

```python
TubuIO.contract.call({
    shortID: "sad1231"
    method: "getCount"
}, {
    args: ["400", "200", "TL"]
})
```

<br>
<br>
<strong> contract.getTransactions(transactionDetails)</strong>
<br>
The method to get the current user's transactions on the specific network using the networkID, shortID, page and page size.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. dict - The ID of the Network, the short ID of the contract, the page and the page size of the transaction that is going to be obtained in <br>

```python
TubuIO.contract.getTransactions({
    networkID: "2"
    shortID: "sad1231"
    page: "1"
    pageSize: "100"
})
```

<br>
<br>
<strong> contract.getTransactionWithHash(transactionHash)</strong>
<br>
The method to get the current user's specific transaction using the transaction hash.
<br>
<br>
<strong>Parameters</strong>
<br>
 1. string - The transaction hash of the specific transaction <br>

```python
TubuIO.contract.update("0xsadasqwe123131")
```


<!-- tabs:end -->

