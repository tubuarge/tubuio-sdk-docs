

### TubuIO.application
<!-- tabs:start -->

### ** Javascript **
**application.create(networkID, appDetails)**
<br>
Creates an application in the network with given networkID using the appDetails
<br>
<br>

**Parameters**
<br>
 1. Number - The ID of the Network that app is going to be created in <br>
 2. Object - The name and description of the app that is going to be created <br>

```js

TubuIO.application.create(8, {
    name: "Sample App"
    description: "Description of the Sample App"
})
```
<br>

**application.getAll(networkID, options)**
<br>
The method to get the current user's applications on the specific network.
<br>
<br>

**Parameters**
<br>
 1. Number - The ID of the Network that app is going to be fetched from <br>
 2. Object - (optional) Query options  <br>

```js

TubuIO.application.getAll(8, {
    page: 3
    pageSize: 34
})
```

<br>

**application.get(networkID, appID)**
<br>
The method to get the current user's specific application on the specific network using the networkID and appID.
<br>
<br>

**Parameters**
<br>
 1. Number - The ID of the Network that app is going to be fetched from <br>
 2. Number - The ID of the Application that is to be queried <br>

```js

TubuIO.application.get(8, 6)
```

<br>

**application.update(networkID, appID, updateDetails)**
<br>
The method to update the current user's specific application on the specific network using the networkID and appID.
<br>
<br>

**Parameters**
<br>
 1. Number - The ID of the Network that app is going to be updated in <br>
 2. Number - The ID of the Application that is to be updated <br>
 3. Object - The new name and description of the app that is going to be updated <br>

```js

TubuIO.application.update(8, 6, {
    name: "Sample App"
    description: "Description of the Sample App"
})
```

<br>

**application.delete(networkID, appID)**
<br>
The method to get the current user's specific application on the specific network using the networkID and appID.
<br>
<br>

**Parameters**
<br>
 1. Number - The ID of the Network that app is going to be deleted from <br>
 2. Number - The ID of the Application that is to be deleted <br>

```js

TubuIO.application.delete(8, 6)
```

### ** Python **

**application.create(networkID, appDetails)**
<br>
Creates an application in the network with given networkID using the appDetails
<br>
<br>

**Parameters**
<br>
1. int - networkID: The network id of the app which is going to be created in <br>
2. dict - appDetails: The detailed information of the application <br>
    1. string - name: The name of the application <br>
    2. string - description: The description of the application <br>

<br>

**Returns**
<br>

1. dict - response : The information of the created application stored in dictionary  <br>
    1. string - message: The application creation status <br>
    2. dict - data: The application data <br>
        1. int - id: The application id <br>
        2. string - name: The application name <br>
        3. string - description: The application description <br>
        4. int - network_id: The network id of the application <br>
        5. int - owner_id: The owner id of the application <br>
        6. string - updated_at: The application update timestamp <br> 
        7. string - created_at: The application create timestamp <br>

**Example**
```python
TubuIO.application.create(
    networkID=8, 
    appDetails={
        name: "Meow"
        description: "Example"
    }
)

> {'message': 'Application created', 'data': {'id': 39, 'name': 'Meow', 'description': 'Example', 'network_id': 8, ..., }}
```

**application.getAll(networkID, options)**
<br>
The method to get the current user's applications on the specific network.
<br>
<br>

**Parameters**
<br>

1. int - networkID: The network id of the apps are going to be queried in <br>
2. dict - options: The options of the page <br>
    1. int - page: The page number of all networks <br>
    2. int - pageSize: The page size of all networks <br>

<br>

**Returns**
<br>

1. array - data : The array of all application dictionaries <br>


**Example**

```python
TubuIO.application.getAll(
    networkID=8, 
    options={
        page: 1,
        pageSize: 100
    }
)

> [{'id': 31, 'name': 'Stars', 'description': 'Channel Contract', 'network_id': 8, 'owner_id': 15, ..., ...}, {...},]

```
<br>

**application.get(networkID, appID)**
<br>
The method to get the current user's specific application on the specific network using the networkID and appID.
<br>
<br>

**Parameters**
<br>
 1. int - networkID: The network id of the specific app which is going to be queried in <br>
 2. int - appID: The application id that is to be queried <br>
 
<br>

**Returns**
<br>
1. dict - data: The application data <br>
    1. int - id: The application id  <br>
    2. string - name: The application name <br>
    3. string - description: The application description <br>
    4. int - network_id: The network id of the application <br>
    5. int - owner_id: The owner id of the application <br>
    6. string - updated_at: The application update timestamp <br> 
    7. string - created_at: The application create timestamp <br>

**Example**
```python

TubuIO.application.get(
    networkID=8, 
    appID=6
)

> {'id': 31, 'name': 'Star', 'description': 'Channel', 'network_id': 8, 'owner_id': 15, ...}

```
<br>

**application.update(networkID, appID, updateDetails)**
<br>
The method to update the current user's specific application on the specific network using the networkID and appID.
<br>
<br>

**Parameters**
<br>
 1. int - networkID: The network id of the specific app which is going to be updated in <br>
 2. int - applicationID: The ID of the application that is to be updated <br>
 3. dict - updateDetails: The new name and description of the app that is going to be updated <br>
    1. string - name: The new application name which is going to be updated <br>
    2. string - description: The new application description which is going to be updated <br>

**Returns**
<br>
1. dict - response : The information of the updated application stored in dictionary  <br>
    1. string - message: The application update status <br>
    2. dict - data: The application data <br>
        1. int - id: The application id <br>
        2. string - name: The updated application name <br>
        3. string - description: The updated application description <br>
        4. int - network_id: The network id of the application <br>
        5. int - owner_id: The owner id of the application <br>
        6. string - updated_at: The application update timestamp <br> 
        7. string - created_at: The application create timestamp <br>

**Example**

```python

TubuIO.application.updateApp(
    networkID=8, 
    appID=6, 
    updateDetails={
        name: "Sample App",
        description: "Description"
    }
)

> {'message': 'Application with 6 id updated', 'data': {'id': 6, 'name': 'Sample App', 'description': 'Description', 'network_id': 8, ...}
```

<br>

**application.delete(networkID, appID)**
<br>
The method to delete the current user's specific application on the specific network using the networkID and appID.
<br>
<br>

**Parameters**
1. int - networkID: The network id of the specific app which is going to be deleted in <br>
2. int - appID: The application id of the app which is going to be deleted <br>

**Returns**
<br>
1. string - status : The status of the deletion of the application <br>

**Example**

```python

TubuIO.application.delete(
    networkID=8, 
    appID=6
)

> "The application 6 is deleted successfully."
```

<!-- tabs:end -->