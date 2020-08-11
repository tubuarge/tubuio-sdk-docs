# TubuIO SDK Documentation
## Installation
<!-- tabs:start -->

#### ** Javascript **

npm install @tubuarge/tubuio

#### ** Python **

pip install tubuio


<!-- tabs:end -->

### Usage

Instance creation and user login is required to use the modules of the SDK
<!-- tabs:start -->

### ** Javascript **

**Instance Creation**
<br>
Creates an instance to interact with the API
<br>
<br>
**Parameters**
<br>
 1. Object <br>
    - urlbase-String: The URL of the API 

```js
const TubuIO = require('@tubuarge/tubuio')
const instance = new TubuIO({
    urlbase: 'https://api-test.tubu.io'
})
```

**TubuIO.login(credentials)**
<br>
Logs in to the API using the username and password
<br>
<br>
**Parameters**
<br>
 1. Object - User credentials for logging in <br>

```js
TubuIO.login({
    username: 'user1',
    password: 'password1'
})
```

### ** Python **

**Instance Creation**
<br>
Creates an instance to interact with the API
<br>
<br>
**Parameters**
<br>
 1. Dictionary <br>
    - urlbase-String: The URL of the API 

```python
tubuio_user =  new TubuIO({
    urlbase: 'https://api-test.tubu.io'
})
```

**TubuIO.login(credentials)**
<br>
Logs in to the API using the username and password
<br>
<br>
**Parameters**
<br>
 1. dict - User credentials stored in dictionary for logging in <br>

```js
tubuio_user.login({
    username: 'user1',
    password: 'password1'
})
```



<!-- tabs:end -->

