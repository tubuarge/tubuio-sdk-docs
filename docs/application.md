

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
<ol>
<li> int - networkID: The network id </li>
<li> dict - appDetails: The detailed information of the application 
<ol> 
<li> string - name: The name of the application </li>
<li> string - description: The description of the application </li>
</ol>
</li>
</ol>

```python

TubuIO.application.create(8, {
    name: "Sample App"
    description: "Description of the Sample App"
})
```
<br>

**Returns**
<br>
<ol>
<li> dict - response : The information of the specific network stored in dictionary 
<ol> 
<li> string - message: The application creation status </li>
<li> dict - data: The application data 
<ol>
<li> int - id: The application id </li>
<li> string - name: The application name </li>
<li> string - description: The application description </li>
<li> int - network_id: The network id of the application </li>
<li> int - owner_id: The owner id of the application </li>
<li> string - updated_at: The network update timestamp </li>
<li> string - created_at: The network create timestamp </li>
</ol>
</li>
</ol>
</li>
</ol>

```python
token = "askdsakdqıoweıq12314.1313qsodlqkldasnd..."
```

**application.getAll(networkID, options)**
<br>
The method to get the current user's applications on the specific network.
<br>
<br>

**Parameters**
<br>
<ol>
<li> int - networkID: The network id of the apps are going to be queried in </li>
<li> dict - options: The options of the page
<ol> 
<li> int - page: The page number of all networks </li>
<li> int - pageSize: The page size of all networks </li>
</ol>
</li>
</ol>
 
```python

TubuIO.application.getAll(8, {
    page: 1,
    pageSize: 100
})
```

<br>

**Returns**
<br>
<ol>
<li> array - data : The array of all application dictionaries </li>
</ol>
 
```python

data = [{'id': 31, 'name': 'Stars', 'description': 'Channel Contract', 'network_id': 2, 'owner_id': 15, ..., ...}, {...},]

```
<br>

**application.getApp(networkID, appID)**
<br>
The method to get the current user's specific application on the specific network using the networkID and appID.
<br>
<br>

**Parameters**
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. int - The ID of the Application that is to be queried <br>

```python

TubuIO.application.getApp(8, 6)
```

<br>

**application.updateApp(networkID, appID, updateDetails)**
<br>
The method to update the current user's specific application on the specific network using the networkID and appID.
<br>
<br>
**Parameters**
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. int - The ID of the Application that is to be queried <br>
 3. dict - The new name and description of the app that is going to be updated <br>

```python

TubuIO.application.updateApp(8, 6, {
    name: "Sample App"
    description: "Description of the Sample App"
})
```

<br>

**application.deleteApp(networkID, appID)**
<br>
The method to get the current user's specific application on the specific network using the networkID and appID.
<br>
<br>
**Parameters**
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. int - The ID of the Application that is to be queried <br>

```python

TubuIO.application.deleteApp(8, 6)
```

<!-- tabs:end -->