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

**Errors**
<br>
1. HTTP - 400: Bad Request with Error Message <br>

### ** Python **

**Instance Creation**
<br>
Creates an instance to interact with the API
<br>
<br>

**Parameters**
<br>
There is no parameter. <br>

**Example**
<br>

```python
tubuio_user =  new TubuIO()
```
<br>

**TubuIO.login(credentials)**
<br>
Logs in to the API using the username and password
<br>
<br>

**Parameters**
<br>
 1. dict - credentials: User credentials stored in dictionary for logging in <br>
    1. string - username: The username of current user <br>
    2. string - password: The password of current user <br>

<br>

**Returns**
<br>
1. string - token: The user token <br>

<br>

**Example**
```python
tubuio_user.login(
    credentials={
        username: 'user1',
        password: 'password1'
    }
)

> "askdsakdqıoweıq12314.1313qsodlqkldasnd..."
```

**Errors**
<br>
1. HTTP - 400: Bad Request with Error Message <br>

<!-- tabs:end -->

