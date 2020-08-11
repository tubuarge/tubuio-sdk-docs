

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

**application.createApp(networkID, appDetails)**
<br>
Creates an application in the network with given networkID using the appDetails
<br>
<br>

**Parameters**
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. dict - The name and description of the app that is going to be created <br>

```python

TubuIO.application.createApp(8, {
    name: "Sample App"
    description: "Description of the Sample App"
})
```
<br>

**application.getApps(networkID, appDetails)**
<br>
The method to get the current user's applications on the specific network.
<br>
<br>

**Parameters**
<br>
 1. int - The ID of the Network that app is going to be created in <br>
 2. dict - The name and description of the app that is going to be created <br>

```python

TubuIO.application.getApps(8, {
    name: "Sample App"
    description: "Description of the Sample App"
})
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