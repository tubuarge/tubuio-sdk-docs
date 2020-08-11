
### TubuIO.contract
<!-- tabs:start -->

### ** Javascript **

**contract.deploy(networkID, contractDetails)**
<br>
Deploys a contract in the network with given networkID using the contractDetails
<br>
<br>

**Parameters**
<br>
 1. Number - The ID of the Network that app is going to be created in <br>
 2. Object - The name, description and application id of the contract that is going to be deployed <br>

```js

TubuIO.contract.deploy(8, {
    name: "Sample App"
    description: "Description of the Sample App"
    appID: "8"
})
```
<br>
<br>

**contract.getAll(networkID, options)**
<br>
The method to get the current user's contracts on the specific network.
<br>
<br>

**Parameters**
<br>
 1. Number - The ID of the Network that app is going to be created in <br>
 2. Object - The page, page size and application id of the contract that is going to be obtained <br>

```js

TubuIO.contract.getAll(8, {
    page: 1
    pageSize: 100
    application_id: 8
})
```

<br>
<br>

**contract.getByShortID(networkID, shortID)**
<br>
The method to get the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
<br>
 1. Number - The networkID  of the contract that is going to be fetched from <br>
 2. String - The shortID of the contract that is going to be fetched <br>


```js

TubuIO.contract.getByShortID(2,"sad1231")
```

<br>
<br>

**contract.delete(networkID, shortID)**
<br>
The method to get the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
<br>
 1. Number - The networkID  of the contract that is going to be deleted <br>
 2. String - The shortID of the contract that is going to be deleted <br>

```js

TubuIO.contract.delete(2,"sad1231")
```

<br>
<br>

**contract.update(networkID, shortID, contractDetails)**
<br>
The method to update the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
<br>
 1. Number - The networkID  of the contract that is going to be updated <br>
 2. String - The shortID of the contract that is going to be updated <br>
 3. Object - The new name and description of the contract <br>

```js
TubuIO.contract.update(2,"sad1231",{
    name: "Sample Name"
    description: "Sample Description"
})
```

<br>
<br>

**contract.invoke(shortID, method, args)**
<br>
The method to invoke the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
<br>
 1. String - The short ID of the contract  <br>
 2. String - The method that is going to be invoked<br>
 3. Object - The args of the method <br>

```js
TubuIO.contract.invoke("sad1231","setCount", {
    args: ["300", "200", "0X1231312asdsadad"]
})
```

<br>
<br>

**contract.call(shortID, method, args)**
The method to call the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
<br>
 1. String - The short ID of the contract  <br>
 2. String - The method that is going to be invoked<br>
 3. Object - The args of the method <br>

```js
TubuIO.contract.call("sad1231","getCount",{
    args: [400, 200, "TL"]
})
```

<br>
<br>

**contract.getTransactions(transactionDetails)**
<br>
The method to get the current user's transactions on the specific network using the networkID, shortID, page and page size.
<br>
<br>

**Parameters**
<br>
 1. Object - The ID of the Network, the short ID of the contract, the page and the page size of the transaction that is going to be obtained in <br>

```js
TubuIO.contract.getTransactions({
    networkID: 2
    shortID: "sad1231"
    page: 1
    pageSize: 100
})
```

<br>
<br>

**contract.getTransactionWithHash(transactionHash)**
<br>
The method to get the current user's specific transaction using the transaction hash.
<br>
<br>

**Parameters**
<br>
 1. string - The transaction hash of the specific transaction <br>

```js
TubuIO.contract.getTransactionWithHash("0xsadasqwe123131")
```

### ** Python **

**contract.deploy(networkID, contractDetails)**
<br>
Deploys a contract in the network with given networkID using the contractDetails
<br>
<br>

**Parameters**
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

**contract.getAll(networkID, pageDetails)**
<br>
The method to get the current user's contracts on the specific network.
<br>
<br>

**Parameters**
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

**contract.getByShortId(contractDetails)**
<br>
The method to get the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
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

**contract.delete(contractDetails)**
<br>
The method to get the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
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

**contract.update(networkDetails, contractDetails)**
<br>
The method to update the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
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

**contract.invoke(contractDetails, args)**
<br>
The method to invoke the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
<br>
 1. dict - The short ID of the contract and the method that is going to be invoked in <br>
 2. dict - The args of the method <br>

```python
TubuIO.contract.invoke({
    shortID: "sad1231"
    method: "setCount"
}, {
    args: ["300", "200", "0X1231312asdsadad"]
})
```

<br>
<br>

**contract.call(networkDetails, contractDetails)**
The method to call the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
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

**contract.getTransactions(transactionDetails)**
<br>
The method to get the current user's transactions on the specific network using the networkID, shortID, page and page size.
<br>
<br>

**Parameters**
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

**contract.getTransactionWithHash(transactionHash)**
<br>
The method to get the current user's specific transaction using the transaction hash.
<br>
<br>

**Parameters**
<br>
 1. string - The transaction hash of the specific transaction <br>

```python
TubuIO.contract.update("0xsadasqwe123131")
```


<!-- tabs:end -->