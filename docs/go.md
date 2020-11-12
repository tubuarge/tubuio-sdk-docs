# Golang SDK

## Get SDK
`go get -u github.com/tubuarge/tubuio-sdk-go/api` <br />


## Create Instance
```go
import(
    tubu "github.com/tubuarge/tubuio-sdk-go/api"
)

func main() {
     app := tubu.NewContract("APIKey")
}
```
#### Parameters
|Param|Type|Required|Description|
|:---:|:---:|:---:|:---:|
| APIKey | string |yes|The API Key of the contract that is obtained from [app.tubu.io](https://app.tubu.io) |

## Contract
```go
    contract := app.CreateNewContract("ShortID")
```

#### Parameters
|Param|Type|Required|Description|
|:---:|:---:|:---:|:---:|
| ShortID | string| yes| The shortID of the contract to be interacted |

### Call

> **contract.Call(shortID, method, tag, account, args)**

Calls the given call method of the contract's given tag version with given args.

#### Parameters

|Param|Type|Required|Description|
|:---:|:---:|:---:|:---:|
|method | string |yes| The method name in the contract to be called |
|tag | string | optinal| The version tag of the contract to be called. If left empty, default contract to be interacted is the latest contract|
|account | string |optinal| Sender account address|
|args | ...interface{} | optinal | The parameters of the method to be called in the contract. If method takes no parameters, pass a nil argument. Note that methods with parameters will not work without arguments|

```go
callResp, err := contract.Call("Method", "Tag", "account", nil)
if err != nil {
    log.Fatal(err)
}

defer callResp.Body.Close()
```

#### Returns
- A **http.Response pointer** from Go's **net/http** package that includes API response as a JSON object that contains data and message. See more [Usage Examples](https://github.com/tubuarge/tubuio-sdk-go/tree/main/examples).

### Send

> **contract.Send(shortID, method, tag, account, args)**

Calls the given send method of the contract's given tag version with given args.

#### Parameters
|Param|Type| Required |Description|
|---|---|---|---|
|method | string | yes| The method name in the contract to be called |
|tag | string | optinal |The version tag of the contract to be called. If left empty, default contract to be interacted is the latest contract|
|account | string | optinal| Sender account address|
|args | ...interface{} | optinal| The parameters of the method to be called in the contract. If method takes no parameters, the default value is null. Note that methods with parameters will not work without arguments|

```go
sendResp, err := contract.Call("Method", "Tag", "Account Address", "item", 123, true)
if err != nil {
    log.Fatal(err)
}

defer sendResp.Body.Close()
```

#### Returns
A **http.Response pointer** from Go's **net/http** package that includes API response as a JSON object that contains data and message. See more [Usage Examples](https://github.com/tubuarge/tubuio-sdk-go/tree/main/examples).
