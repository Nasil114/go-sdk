# \DefaultAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**SumGet**](DefaultAPI.md#SumGet) | **Get** /sum | Add two numbers



## SumGet

> int32 SumGet(ctx).A(a).B(b).Execute()

Add two numbers

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "github.com/Nasil114/go-sdk"
)

func main() {
    a := int32(56) // int32 | 
    b := int32(56) // int32 | 

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.DefaultAPI.SumGet(context.Background()).A(a).B(b).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DefaultAPI.SumGet``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `SumGet`: int32
    fmt.Fprintf(os.Stdout, "Response from `DefaultAPI.SumGet`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSumGetRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **a** | **int32** |  | 
 **b** | **int32** |  | 

### Return type

**int32**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

