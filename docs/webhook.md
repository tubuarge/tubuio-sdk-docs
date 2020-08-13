

### TubuIO.webhook
<!-- tabs:start -->

### ** Javascript **
**webhook.create(webhookDetails)**
<br>
Creates a webhook using the webhookDetails.
<br>
<br>

**Parameters**
<br>
1. Object - webhookDetails: The detailed information of the webhook <br>
    1. String - name: The name of the webhook <br>
    2. String - description: The description of the webhook <br>
    3. String - url: The url of the webhook <br>
    4. Object - authorization: The authorization token of the webhook <br>
    5. String - shortID: The short id of the contract <br>
<br>

**Returns**
<br>

1. Object - response : The information of the created webhook stored in Object  <br>
    1. String - message: The webhook creation status <br>
    2. Object - data: The webhook data <br>
        1. int - id: The webhook id <br>
        2. String - name: The webhook name <br>
        3. String - description: The webhook description <br>
        4. String - contract_address: The address of the contract <br>
        5. String - short_id: The short id of the contract
        6. String - updated_at: The application update timestamp <br> 
        7. String - created_at: The application create timestamp <br>
        8. String - abi: Application Binary Interface of the contract <br>
        9. String - owner_address: The address of the contract owner <br>
        10. String - user_id: The id of user <br>

**Example**
```js
TubuIO.webhook.create({
    name: "Meow",
    description: "Example",
    url: "http://www.tubu.io",
    authorization: {},
    shortID: "sadqwe123"
})

> {'message': 'Webhook created', 'data': {'id': 39, 'name': 'Meow', 'description': 'Example', 'contract_address': "0xsdwqe1e123asd1", ..., }}
```

**webhook.getAll(shortID)**
<br>
The method to get the contract's webhook using the short id of the contract.
<br>
<br>

**Parameters**
<br>

1. String - shortID: The short id of the contract <br>

<br>

**Returns**
<br>

1. array - data : The array of all webhook objects <br>


**Example**

```js
TubuIO.webhook.getAll("sadqwe123")

> [{'id': 39, 'name': 'Meow', 'description': 'Example', 'contract_address': "0xsdwqe1e123asd1", ..., }, {...},]

```
<br>

**webhook.get(webhookID)**
<br>
The method to get the current user's specific webhook using webhookID.
<br>
<br>

**Parameters**
<br>
 1. int - webhookID: The id of the webhook which is going to be queried in <br>
 
<br>

**Returns**
<br>
1. Object - data: The webhook data <br>
    1. int - id: The webhook id <br>
    2. String - name: The webhook name <br>
    3. String - description: The webhook description <br>
    4. String - contract_address: The address of the contract <br>
    5. String - short_id: The short id of the contract
    6. String - updated_at: The application update timestamp <br> 
    7. String - created_at: The application create timestamp <br>
    8. String - abi: Application Binary Interface of the contract <br>
    9. String - owner_address: The address of the contract owner <br>
    10. String - user_id: The id of user <br>


**Example**
```js

TubuIO.webhook.get(39)

> {'id': 39, 'name': 'Meow', 'description': 'Example', 'contract_address': "0xsdwqe1e123asd1", ..., }

```
<br>

### ** Python **

**webhook.create(webhookDetails)**
<br>
Creates a webhook using the webhookDetails.
<br>
<br>

**Parameters**
<br>
1. dict - webhookDetails: The detailed information of the webhook <br>
    1. string - name: The name of the webhook <br>
    2. string - description: The description of the webhook <br>
    3. string - url: The url of the webhook <br>
    4. dict - authorization: The authorization token of the webhook <br>
    5. string - shortID: The short id of the contract <br>
<br>

**Returns**
<br>

1. dict - response : The information of the created webhook stored in dictionary  <br>
    1. string - message: The webhook creation status <br>
    2. dict - data: The webhook data <br>
        1. int - id: The webhook id <br>
        2. string - name: The webhook name <br>
        3. string - description: The webhook description <br>
        4. string - contract_address: The address of the contract <br>
        5. string - short_id: The short id of the contract
        6. string - updated_at: The application update timestamp <br> 
        7. string - created_at: The application create timestamp <br>
        8. string - abi: Application Binary Interface of the contract <br>
        9. string - owner_address: The address of the contract owner <br>
        10. string - user_id: The id of user <br>

**Example**
```python
TubuIO.webhook.create(
    webhookDetails={
        name: "Meow",
        description: "Example",
        url: "http://www.tubu.io",
        authorization: {},
        shortID: "sadqwe123"
    }
)

> {'message': 'Webhook created', 'data': {'id': 39, 'name': 'Meow', 'description': 'Example', 'contract_address': "0xsdwqe1e123asd1", ..., }}
```

**webhook.getAll(shortID)**
<br>
The method to get the contract's webhook using the short id of the contract.
<br>
<br>

**Parameters**
<br>

1. string - shortID: The short id of the contract <br>

<br>

**Returns**
<br>

1. array - data : The array of all webhook dictionaries <br>


**Example**

```python
TubuIO.webhook.getAll(
    shortID="sadqwe123", 
)

> [{'id': 39, 'name': 'Meow', 'description': 'Example', 'contract_address': "0xsdwqe1e123asd1", ..., }, {...},]

```
<br>

**webhook.get(webhookID)**
<br>
The method to get the current user's specific webhook using webhookID.
<br>
<br>

**Parameters**
<br>
 1. int - webhookID: The id of the webhook which is going to be queried in <br>
 
<br>

**Returns**
<br>
1. dict - data: The webhook data <br>
    1. int - id: The webhook id <br>
    2. string - name: The webhook name <br>
    3. string - description: The webhook description <br>
    4. string - contract_address: The address of the contract <br>
    5. string - short_id: The short id of the contract
    6. string - updated_at: The application update timestamp <br> 
    7. string - created_at: The application create timestamp <br>
    8. string - abi: Application Binary Interface of the contract <br>
    9. string - owner_address: The address of the contract owner <br>
    10. string - user_id: The id of user <br>


**Example**
```python

TubuIO.webhook.get(
    webhookID=39
)

> {'id': 39, 'name': 'Meow', 'description': 'Example', 'contract_address': "0xsdwqe1e123asd1", ..., }

```
<br>

<!-- tabs:end -->