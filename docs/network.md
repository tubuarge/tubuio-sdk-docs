
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
<ol>
<li> dict - options: The options of the page
<ol> 
<li> int - page: The page number of all networks </li>
<li> int - pageSize: The page size of all networks </li>
</ol>
</li>
</ol>

```python

TubuIO.network.getAll({
    page: 1,
    pageSize: 100
})

```
<br>

**Returns**
<br>
<ol>
<li> array - data : The array of all network dictionaries </li>
</ol>
 
```python

data = [{'id': 1, 'name': 'Test Quorum Network', 'bctype': 'Quorum', 'consensus': 'raft', ... , 'version': '2.3.0', ...}, {...}, ...]

```
<br>
<br>

**network.get(networkID)**
<br>
Fetches the network of the user with the given ID 
<br>
<br>

**Parameters**
<br>
<ol>
<li> int - networkID: The ID of the Network that is going to be fetched </li>
</ol>

```python

network = TubuIO.network.get(14)

```

<br>

**Returns**
<br>
<ol>
<li> dict - data : The information of the specific network stored in dictionary 
<ol> 
<li> int - id: The network id </li>
<li> string - name: The network name </li>
<li> string - bctype: The network blockchain type </li>
<li> string - version: The network blockchain version </li>
<li> string - consensus: The network consensus type </li>
<li> string - ip_address: The network ip address </li>
<li> int - ws_port: The network ws port </li>
<li> bool - is_public: The network blockchain access type </li>
<li> int - owner_id: The owner id </li>
<li> string - updated_at: The network update timestamp </li>
<li> string - created_at: The network create timestamp </li>
<li> dict - chain : The information of the specific network stored in dictionary 
<ol>
<li> int - blockCount: The block count of the blockchain </li>
<li> int - chainId: The blockchain id </li>
<li> string - nodeInfo: The information of blockchain </li>
</ol>
</li>
</ol>
</li>
</ol>
 
```python

data = {'id': 2, 'name': 'TUBU - Quorum Network', 'bctype': 'Quorum', 'version': '2.6.0', ..., 'chain': {...}}}

```
<br>
<br>

<!-- tabs:end -->