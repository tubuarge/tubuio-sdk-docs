
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

**Errors**
<br>
1. HTTP - 400: Error <br>
2. HTTP - 404: Not Found <br>

**network.get(networkID)**
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
<br>

**Errors**
<br>
1. HTTP - 400: Error <br>
2. HTTP - 404: Not Found <br>
3. HTTP - 405: Validation Exception <br>


### ** Python **

**network.getAll(options)**
<br>
Fetches all the networks of the current user
<br>
<br>


**Parameters**
<br>
1. dict - options: The options of the page <br>
    1. int - page: The page number of all networks <br> 
    2. int - pageSize: The page size of all networks <br>

<br>

**Returns**
<br>
1. array - data : The array of all network dictionaries <br>

**Example**

```python

TubuIO.network.getAll(
    options={
        page: 1,
        pageSize: 100
    }
)

> [{'id': 1, 'name': 'Test Quorum Network', 'bctype': 'Quorum', 'consensus': 'raft', ... , 'version': '2.3.0', ...}, {...}, ...]

```

<br>
**Errors**
<br>
1. HTTP - 400: Error <br>
2. HTTP - 404: Not Found <br>

<br>
<br>

**network.get(networkID)**
<br>
Fetches the network of the user with the given ID 
<br>
<br>

**Parameters**
<br>
1. int - networkID: The ID of the Network that is going to be fetched <br>
<br>

**Returns**
<br>

1. dict - data : The information of the specific network stored in dictionary <br>
    1. int - id: The network id <br>
    2. string - name: The network name <br>
    3. string - bctype: The network blockchain type <br>
    4. string - version: The network blockchain version <br>
    5. string - consensus: The network consensus type <br>
    6. string - ip_address: The network ip address <br>
    7. int - ws_port: The network ws port <br> 
    8. bool - is_public: The network blockchain access type <br>
    9. int - owner_id: The owner id <br>
    10. string - updated_at: The network update timestamp <br>
    11. string - created_at: The network create timestamp <br>
    12. dict - chain : The information of the specific network stored in dictionary <br>
        1. int - blockCount: The block count of the blockchain <br>
        2. int - chainId: The blockchain id <br>
        3. string - nodeInfo: The information of blockchain <br>

**Example**
```python

TubuIO.network.get(
    networkID=14
)

> {'id': 14, 'name': 'TUBU - Quorum Network', 'bctype': 'Quorum', 'version': '2.6.0', ..., 'chain': {...}}}

```
<br>

**Errors**
<br>
1. HTTP - 400: Error <br>
2. HTTP - 404: Not Found <br>
3. HTTP - 405: Validation Exception <br>

<!-- tabs:end -->