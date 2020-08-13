
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
 1. int - networkID: The network id of the contract is going to be deployed in <br>
 2. dict - contractDetails:  The detailed information of the contract <br>
    1. string - name: The name of the contract <br>
    2. string - description: The description of the contract <br>
    3. int - appID: The application id of the contract which is going to be deployed in <br>
    4. array - files: The filepath of the contracts which is stored in an array <br>
    5. array - args: The args of the contract <br>

**Returns**
<br>

1. dict - response : The information of the deployed contract stored in dictionary  <br>
    1. string - message: The contract deploy status <br>
    2. dict - data: The contract data <br>
        1. int - id: The contract id <br>
        2. string - name: The contract name <br>
        3. string - description: The contract description <br>
        4. string - short_id: The short id of the contract <br>
        5. string - contract_address: The owner id of the application <br>
        6. string - updated_at: The contract update timestamp <br>
        7. string - created_at: The contract create timestamp <br>

**Example**
<br>

```python
TubuIO.contract.deploy(networkID=8, {
    name: "Stars.sol",
    description: "Description",
    appID: 8,
    files: ["..\\contracts\\Stars.sol", ...],
    args: "Contract",
})

> {'message': 'Contract created', 'data': {'id': 60, 'name': 'Stars.sol', 'description': 'Description', 'short_id': '1d81c392a3cd',...}}
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
 1. int - networkID: The network id of the contract is going to be deployed in <br>
 2. dict - pageDetails:  The detailed information of the page <br>
    1. int - page: The page number of the contracts <br>
    2. int - pageSize: The page size of the contracts <br>
    3. int - appID: The application id of the contracts <br>


**Returns**
<br>

1. array - data : The array of all contract dictionaries <br>

**Example**
<br>

```python

TubuIO.contract.getAll(8, {
    page: 1,
    page_size: 100,
    app_id: 8,
})

> [{'id': 42, 'name': 'Stars.sol', 'description': 'Channel Contract', 'short_id': 'e0e9fa97dac2', ...}, {...}, ...]
```


<br>
<br>

**contract.get(networkID, shortID)**
<br>
The method to get the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
<br>
 1. int - networkID: The network id of the contract is going to be deployed in <br>
 2. string - shortID: The short id of the contract <br>

**Returns**
<br>

1. dict - data : The array of all contract dictionaries <br>
    1. int - id: The contract id <br>
    2. string - name: The name of the contract <br>
    3. string - description: The description of the contract <br>
    4. array - abi: Application Binary Interface of the contract <br>
    5. string - bytecode: The bytecode of the contract
    6. dict - args: The arguments of the contract <br>
    7. dict - metadata: Metadata of the contract <br>
    8. string - short_id: The short id of the contract <br>
    9. string - contract-address: The address of the contract <br>
    10. string - owner_address: The address of the contract owner <br>
    11. string - owner_privatekey: The private key of the contract owner <br>
    12. int - application_id: The application id of the contract <br>
    13. int - network_id: The network id of the contract <br>
    14. int - owner_id: The id of the contract owner <br>
    15. string - created_at: The timestamp of the created contract <br>
    16. string - updated_at: The timestamp of the updated contract <br>

**Example**
<br>

```python

TubuIO.contract.get(
    networkID=2,
    shortID="sad1231"
)

> {'id': 42, 'name': 'Omercik.sol', 'description': 'Yesilcam', 'abi': [...], 'args': {...}, ..., 'metadata': {...}, ...}
```

<br>
<br>

**contract.delete(networkID, shortID)**
<br>
The method to delete the current user's specific contract on the specific network using the networkID and shortID.
<br>
<br>

**Parameters**
<br>
1. int - networkID: The network id of the contract is going to be deployed in <br>
2. string - shortID: The short id of the contract <br>

**Returns**
<br>
1. string - status : The status of the deletion of the contract  <br>

**Example**

```python

TubuIO.contract.delete({
    networkID: 2,
    shortID: "sad1231"
})

> "The contract sad1231 is deleted successfully."
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
1. int - networkID: The network id of the contract is going to be deployed in <br>
2. string - shortID: The short id of the contract <br>
3. dict - contractDetails: The detailed information of the contract which is going to be updated. <br>
    1. string - name: The name of the contract <br>
    2. string - description: The description of the contract <br>

**Returns**
<br>
1. dict - response : The information of the updated contract stored in dictionary  <br>
    1. string - message: The contract update status <br>
    2. dict - data: The contract data <br>
        1. int - id: The contract id <br>
        2. string - name: The name of the contract <br>
        3. string - description: The description of the contract <br>
        4. array - abi: Application Binary Interface of the contract <br>
        5. dict - args: The arguments of the contract <br>
        6. dict - metadata: Metadata of the contract <br>
        7. string - short_id: The short id of the contract <br>
        8. string - contract-address: The address of the contract <br>
        9. string - owner_address: The address of the contract owner <br>
        10. string - owner_privatekey: The private key of the contract owner <br>
        11. int - application_id: The application id of the contract <br>
        12. int - network_id: The network id of the contract <br>
        13. int - owner_id: The id of the contract owner <br>
        14. string - created_at: The timestamp of the created contract <br>
        15. string - updated_at: The timestamp of the updated contract <br>

**Example**

```python
TubuIO.contract.update(
    networkID=2,
    shortID="sad1231",
    contractDetails={
        name: "Name.sol",
        description: "Description"
    }
)

> {'message': 'Contract with e0e9fa97dac2 id updated',{'id': 42, 'name': 'Name.sol', 'description': 'Description', ..., ...}}
```

<br>
<br>

**contract.invoke(shortID, method, args)**
<br>
The method to invoke the current user's specific contract on the specific network using the shortID.
<br>
<br>

**Parameters**
<br>
 1. string - shortID: - The short ID of the contract and the method that is going to be invoked in <br>
 2. string - method: - The method name of the contract. <br>
 3. dict - args: The args of the method <br>

**Returns**
<br>
1. dict - data: The contract invoke data <br>
    1. string - blockHash: The blockhash of the block <br>
    2. int - blockNumber: The number of the block <br>
    3. string - contractAddress: The address of the contract <br>
    4. int - cumulativeGasUsed: The cumulative gas used <br>
    5. string - from: The address of the sender <br>
    6. int - gasUsed: The used gas amount <br>
    7. string - logsBloom: The logs bloom <br>
    8. bool - status: The status of the invoke <br>
    9. string - to: The address of the receiver <br>
    10. string - transactionHash: The hash of the transaction <br>
    11. int - transactionIndex: The index of the transaction <br>
    12. dict - events: The events of the contract <br>

**Example**

```python
TubuIO.contract.invoke(
    shortID="sad1231",
    method="setCount",
    args={
        args: ["300", "200", "0X1231312asdsadad"]
    }
)

> {'data': {'blockHash': '0x32b8bbfe10dcd34918b41cdc6e7...', 'blockNumber': 164, 'contractAddress': None, ..., 'gasUsed': 26748, ...} 
```

<br>
<br>

**contract.call(shortID, method, contractDetails)**
The method to call the function of the current user's specific contract on the specific network using the shortID.
<br>
<br>

**Parameters**
<br>
1. string - shortID: - The short ID of the contract and the method that is going to be invoked in <br>
2. string - method: - The method name of the contract. <br>
3. dict - args: The args of the method <br>

**Returns**
<br>
1. dict - data: The contract call result <br>

**Example**
```python
TubuIO.contract.invoke(
    shortID="sad1231",
    method="setCount",
    args={
        args: ["300", "200", "0X1231312asdsadad"]
    }
)

>  {'data': '400'}
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
 1. dict - transactionDetails: The details of the transactions <br>
    1. int - networkID: The network id of the contract is going to be deployed in <br>
    2. string - shortID: The short id of the contract <br>
    3. int - page: The page number of the transactions <br>
    4. int - pageSize: The page size of the transactions <br>

**Returns**
<br>
1. dict - data: The transaction dictionary <br>
    1. string - message: The transaction found message <br>
    2. dict - meta: The transaction meta <br>
    3. dict - data: Array of the transactions information <br>


**Example**
```python
TubuIO.contract.getTransactions({
    networkID: 2,
    shortID: "sad1231",
    page: 1,
    pageSize: 100
})

> {'message': 'Transaction listed', 'meta': {'totalCount': 27, 'totalPage': 2, 'page': 1}, 'data':[...]}
```

<br>
<br>

**contract.getTransaction(transactionHash)**
<br>
The method to get the current user's specific transaction using the transaction hash.
<br>
<br>

**Parameters**
<br>
 1. string - The transaction hash of the specific transaction <br>

 **Returns**
 <br>
 1. dict - response : The information of the transaction with the given hash stored in dictionary  <br>
    1. string - message: The transaction query status <br>
    2. dict - data: The transaction data <br>
        1. int - id: The transaction id <br>
        2. int - user_id: The id of the user <br>
        3. string - short_id: The short id of the contract <br>
        4. string - block_hash: The hash of the block <br>
        5. int - block_number: The id of the block <br>
        6. string - from_address: The address of sender of the transaction <br>
        7. string - hash: The hash of the transaction <br>
        8. array - input: The input of the contract <br>
        9. bool - status: The status of the transaction <br>
        10. string - to_address: The address of receiver of the transaction <br>
        11. dict - extra_data: The extra data of the transaction <br>
            1. int - gasUsed: The used gas amount <br>
            2. int - cumulativeGasUsed: The cumulative gas used <br>
            3. dict - events: The events of the contract <br>
        12. string - created_at: The timestamp of the created contract <br>
        13. string - updated_at: The timestamp of the updated contract <br>

**Example**    

```python
TubuIO.contract.getTransaction(
    transactionHash="0xsadasqwe123131"
)

> {'message': 'Transaction found', 'data': {'id': 71, 'user_id': 15, 'short_id': 'e6da40e5bc87', ...}}
```


<!-- tabs:end -->