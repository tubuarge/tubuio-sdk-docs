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

pip install tubuio


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

pip install tubuio


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

pip install tubuio


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

pip install tubuio


<!-- tabs:end -->