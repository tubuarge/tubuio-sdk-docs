
## TubuIO.network
The module that is used to interact with the networks in TubuIO

<!-- tabs:start -->

### ** Javascript **
**network.getAll(options)**
<br>
Fetches all the networks of the current user
<br>
<br>

**Parameters**
<br>
 1. Object - (optional) Query options<br>


```js

TubuIO.network.getAll({
    page: 1,
    pageSize: 100
})

```
<br>
<br>

**network.getByID(networkID)**
<br>
Fetches the network of the user with the given ID 
<br>
<br>

**Parameters**
<br>
 1. Number - The ID of the Network that is going to be fetched <br>

```js

TubuIO.network.getByID(14)

```
### ** Python **

**network.getAll(options)**
<br>
Fetches all the networks of the current user
<br>
<br>


**Parameters**
<br>
 1. dict - (optional) Query options<br>


```python

TubuIO.network.getAll({
    page: 1,
    pageSize: 100
})

```
<br>
<br>

**network.getByID(networkID)**
<br>
Fetches the network of the user with the given ID 
<br>
<br>

**Parameters**
<br>
 1. int - The ID of the Network that is going to be fetched <br>

```python

TubuIO.network.getByID(14)

```


<!-- tabs:end -->