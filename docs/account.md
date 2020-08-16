

### TubuIO.contractAccount
<!-- tabs:start -->

### ** Javascript **

**contractAddress.create(accountDetails)**
<br>
Creates a contract account using the accountDetails.
<br>
<br>

**Parameters**
<br>
1. String - shortID: The short id of the contract <br>
2. Object - webhookDetails: The detailed information of the webhook <br>
    1. String - name: The name of the contract account <br>
<br>

**Returns**
<br>

1. Object - response : The information of the created contract account stored in dictionary  <br>
    1. String - message: The contract account creation status <br>
    2. Object - data: The contract account data <br>
        1. Number - id: The contract account id <br>
        2. String - name: The contract account name <br>
        3. String - address: The contract account address <br>
        4. Boolean - is_active: The activation status of the contract account <br>
        5. String - updated_at: The contract account update timestamp <br> 
        6. String - created_at: The contract account create timestamp <br>

**Example**
```js
TubuIO.contractAccount.create(shortID='f01bee72e037',
    accountDetails={
        name: "Main"
    }
)

> {'message': 'Contract Account created', 'data': {'id': 13, 'name': 'Main', 'address': '0xd7e55358Bfb1f...', 'is_active': True, ...}}
```

<br>

**Errors**
<br>
1. HTTP - 400: Bad Request with Error Message <br>
2. HTTP - 405: Validation Exception <br>

**contractAddress.getAll(shortID, options)**
<br>
The method to get the contract addresses using the short id of the contract.
<br>
<br>

**Parameters**
<br>

1. String - shortID: The short id of the contract <br>
2. Object - options: The options of the page <br>
    1. Number - page: The page number of all networks <br>
    2. Number - pageSize: The page size of all networks <br>


<br>

**Returns**
<br>

1. Object - data : The array of all contract address dictionaries <br>


**Example**

```js
TubuIO.contractAccount.getAll(
    shortID="sadqwe123",
    options={
        page: 1,
        pageSize: 100
    }
)

> [{'id': 2, 'name': 'Main', 'address': '0xA157d64e25c7b37D42Ea7c2714abE41D7E185a46', 'is_active': True, ...}, {...}, ...]

```

<br>

**Errors**
<br>
1. HTTP - 400: Error <br>
2. HTTP - 404: Not Found <br>
3. HTTP - 405: Validation Exception <br>


**contractAccount.get(shortID, accountID)**
<br>
The method to get the current user's specific webhook using webhookID.
<br>
<br>

**Parameters**
<br>
 1. String - shortID: The short id of the contract <br>
 2. Number - accountID: The id of the contract account which is going to be queried in <br>
 
<br>

**Returns**
<br>
1. Object - data: The contract account data <br>
    1. Number - id: The contract account id <br>
    2. String - name: The contract account name <br>
    3. String - address: The contract account address <br>
    4. String - private_key: The private key of the contract address <br>
    5. Boolean - is_active: The activation status of the contract account <br>
    6. String - short_id: The short id of the contract
    7. String - updated_at: The contract account update timestamp <br> 
    8. String - created_at: The contract account create timestamp <br>


**Example**
```js

TubuIO.contractAccount.get(
    shortID='70cb39d78cc4',
    accountID=2
)

> {'id': 2, 'name': 'Main', 'address': '...', 'private_key': '...', 'is_active': True, ...}

```

<br>

**Errors**
<br>
1. HTTP - 400: Error <br>
2. HTTP - 404: Not Found <br>
3. HTTP - 405: Validation Exception <br>



### ** Python **

**contractAddress.create(accountDetails)**
<br>
Creates a contract account using the accountDetails.
<br>
<br>

**Parameters**
<br>
1. string - shortID: The short id of the contract <br>
2. dict - webhookDetails: The detailed information of the webhook <br>
    1. string - name: The name of the contract account <br>
<br>

**Returns**
<br>

1. dict - response : The information of the created contract account stored in dictionary  <br>
    1. string - message: The contract account creation status <br>
    2. dict - data: The contract account data <br>
        1. int - id: The contract account id <br>
        2. string - name: The contract account name <br>
        3. string - address: The contract account address <br>
        4. bool - is_active: The activation status of the contract account <br>
        5. string - updated_at: The contract account update timestamp <br> 
        6. string - created_at: The contract account create timestamp <br>

**Example**
```python
TubuIO.contractAccount.create(shortID='f01bee72e037',
    accountDetails={
        name: "Main"
    }
)

> {'message': 'Contract Account created', 'data': {'id': 13, 'name': 'Main', 'address': '0xd7e55358Bfb1f...', 'is_active': True, ...}}
```

<br>

**Errors**
<br>
1. HTTP - 400: Bad Request with Error Message <br>
2. HTTP - 405: Validation Exception <br>

**contractAddress.getAll(shortID, options)**
<br>
The method to get the contract addresses using the short id of the contract.
<br>
<br>

**Parameters**
<br>

1. string - shortID: The short id of the contract <br>
2. dict - options: The options of the page <br>
    1. int - page: The page number of all networks <br>
    2. int - pageSize: The page size of all networks <br>


<br>

**Returns**
<br>

1. array - data : The array of all contract address dictionaries <br>


**Example**

```python
TubuIO.contractAccount.getAll(
    shortID="sadqwe123",
    options={
        page: 1,
        pageSize: 100
    }
)

> [{'id': 2, 'name': 'Main', 'address': '0xA157d64e25c7b37D42Ea7c2714abE41D7E185a46', 'is_active': True, ...}, {...}, ...]

```

<br>

**Errors**
<br>
1. HTTP - 400: Error <br>
2. HTTP - 404: Not Found <br>
3. HTTP - 405: Validation Exception <br>


**contractAccount.get(shortID, accountID)**
<br>
The method to get the current user's specific webhook using webhookID.
<br>
<br>

**Parameters**
<br>
 1. string - shortID: The short id of the contract <br>
 2. int - accountID: The id of the contract account which is going to be queried in <br>
 
<br>

**Returns**
<br>
1. dict - data: The contract account data <br>
    1. int - id: The contract account id <br>
    2. string - name: The contract account name <br>
    3. string - address: The contract account address <br>
    4. string - private_key: The private key of the contract address <br>
    5. bool - is_active: The activation status of the contract account <br>
    6. string - short_id: The short id of the contract
    7. string - updated_at: The contract account update timestamp <br> 
    8. string - created_at: The contract account create timestamp <br>


**Example**
```python

TubuIO.contractAccount.get(
    shortID='70cb39d78cc4',
    accountID=2
)

> {'id': 2, 'name': 'Main', 'address': '...', 'private_key': '...', 'is_active': True, ...}

```

<br>

**Errors**
<br>
1. HTTP - 400: Error <br>
2. HTTP - 404: Not Found <br>
3. HTTP - 405: Validation Exception <br>


<!-- tabs:end -->