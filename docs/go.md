# Golang SDK

## Get SDK
`go get github.com/tubuarge/tubuio-sdk-go/api`
`go get github.com/tubuarge/tubuio-sdk-go/util`


## Create Instance
```go
import(
    tubu "github.com/tubuarge/tubuio-sdk-go"
)

func main() {
     apiStruct := tubu.NewApiStruct("APIKey")
}
```
#### Parameters
|Param|Type|Required|Description|
|:---:|:---:|:---:|:---:|
| APIKey | string |yes|The API Key of the contract that is obtained from [app.tubu.io](https://app.tubu.io) |


### Call

> **apiStruct.Call(shortID, method, tag, account, args)**

Calls the given call method of the contract's given tag version with given args.

#### Parameters

|Param|Type|Required|Description|
|:---:|:---:|:---:|:---:|
|shortID | string |yes |The shortID of the contract to be interacted |
|method | string |yes| The method name in the contract to be called |
|tag | string | optinal| The version tag of the contract to be called. If left empty, default contract to be interacted is the latest contract|
|account | string |optinal| Sender account address|
|args | ...interface{} | optinal | The parameters of the method to be called in the contract. If method takes no parameters, pass a nil argument. Note that methods with parameters will not work without arguments|

```go
callResp, err := apiStruct.Call("Contract ShortId", "Method", "Tag", "")
if err != nil {
    log.Fatal(err)
}

defer callResp.Body.Close()
```

#### Returns
- A **http.Response pointer** from Go's **net/http** package that includes API response as a JSON object that contains data and message. See more [Usage Examples](https://github.com/tubuarge/tubuio-sdk-go/tree/main/examples).

### Send

> **apiStruct.Send(shortID, method, tag, account, args)**

Calls the given send method of the contract's given tag version with given args.

#### Parameters
|Param|Type| Required |Description|
|---|---|---|---|
|shortID | string | yes|The shortID of the contract to be interacted |
|method | string | yes| The method name in the contract to be called |
|tag | string | optinal |The version tag of the contract to be called. If left empty, default contract to be interacted is the latest contract|
|account | string | optinal| Sender account address|
|args | ...interface{} | optinal| The parameters of the method to be called in the contract. If method takes no parameters, the default value is null. Note that methods with parameters will not work without arguments|

```go
sendResp, err := apiStruct.Call("Contract ShortId", "Method", "Tag", "Account Address", "item", 123, true)
if err != nil {
    log.Fatal(err)
}

defer sendResp.Body.Close()
```

#### Returns
A **http.Response pointer** from Go's **net/http** package that includes API response as a JSON object that contains data and message. See more [Usage Examples](https://github.com/tubuarge/tubuio-sdk-go/tree/main/examples).

