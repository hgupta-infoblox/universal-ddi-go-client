# PassiveDiscoveryConfigServiceAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Create**](PassiveDiscoveryConfigServiceAPI.md#Create) | **Post** /api/discovery/v1/passive_discovery_config/{id} | Create the PassiveDiscoveryConfig object. Use this method to create the PassiveDiscoveryConfig object.
[**ListPassiveDiscoveryAccounts2**](PassiveDiscoveryConfigServiceAPI.md#ListPassiveDiscoveryAccounts2) | **Get** /api/discovery/v1/passive_discovery_config/{source}/accounts | List account by enabled source. Use this method to retrieve a list of enabled account that have the given source. The response format is an object containing a list of account ID objects.
[**Read**](PassiveDiscoveryConfigServiceAPI.md#Read) | **Get** /api/discovery/v1/passive_discovery_config/{id} | Read the PassiveDiscoveryConfig object. Use this method to read the PassiveDiscoveryConfig object.
[**Update**](PassiveDiscoveryConfigServiceAPI.md#Update) | **Patch** /api/discovery/v1/passive_discovery_config/{id} | Update the PassiveDiscoveryConfig object. Use this method to update the PassiveDiscoveryConfig object.



## Create

> ControllerCreatePassiveDiscoveryConfigResponse Create(ctx, id).Body(body).Execute()

Create the PassiveDiscoveryConfig object. Use this method to create the PassiveDiscoveryConfig object.

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"

	"github.com/infobloxopen/universal-ddi-go-client/discoverycontroller"
)

func main() {
	id := "a5183192-1e00-475f-b334-38e1f0bb1bc7" // string | An application specific resource identity of a resource
	body := *discoverycontroller.NewControllerPassiveDiscoveryConfig() // ControllerPassiveDiscoveryConfig | 

	apiClient := discoverycontroller.NewAPIClient()
	resp, r, err := apiClient.PassiveDiscoveryConfigServiceAPI.Create(context.Background(), id).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PassiveDiscoveryConfigServiceAPI.Create``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `Create`: ControllerCreatePassiveDiscoveryConfigResponse
	fmt.Fprintf(os.Stdout, "Response from `PassiveDiscoveryConfigServiceAPI.Create`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | An application specific resource identity of a resource | 

### Other Parameters

Other parameters are passed through a pointer to a `PassiveDiscoveryConfigServiceAPICreateRequest` struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**body** | [**ControllerPassiveDiscoveryConfig**](ControllerPassiveDiscoveryConfig.md) |  | 

### Return type

[**ControllerCreatePassiveDiscoveryConfigResponse**](ControllerCreatePassiveDiscoveryConfigResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListPassiveDiscoveryAccounts2

> ControllerListPassiveDiscoveryAccountsResponse ListPassiveDiscoveryAccounts2(ctx, source).Execute()

List account by enabled source. Use this method to retrieve a list of enabled account that have the given source. The response format is an object containing a list of account ID objects.

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"

	"github.com/infobloxopen/universal-ddi-go-client/discoverycontroller"
)

func main() {
	source := TODO // interface{} | 

	apiClient := discoverycontroller.NewAPIClient()
	resp, r, err := apiClient.PassiveDiscoveryConfigServiceAPI.ListPassiveDiscoveryAccounts2(context.Background(), source).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PassiveDiscoveryConfigServiceAPI.ListPassiveDiscoveryAccounts2``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListPassiveDiscoveryAccounts2`: ControllerListPassiveDiscoveryAccountsResponse
	fmt.Fprintf(os.Stdout, "Response from `PassiveDiscoveryConfigServiceAPI.ListPassiveDiscoveryAccounts2`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**source** | [**interface{}**](.md) |  | 

### Other Parameters

Other parameters are passed through a pointer to a `PassiveDiscoveryConfigServiceAPIListPassiveDiscoveryAccounts2Request` struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

### Return type

[**ControllerListPassiveDiscoveryAccountsResponse**](ControllerListPassiveDiscoveryAccountsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## Read

> ControllerReadPassiveDiscoveryConfigResponse Read(ctx, id).Fields(fields).Execute()

Read the PassiveDiscoveryConfig object. Use this method to read the PassiveDiscoveryConfig object.

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"

	"github.com/infobloxopen/universal-ddi-go-client/discoverycontroller"
)

func main() {
	id := "a5183192-1e00-475f-b334-38e1f0bb1bc7" // string | An application specific resource identity of a resource

	apiClient := discoverycontroller.NewAPIClient()
	resp, r, err := apiClient.PassiveDiscoveryConfigServiceAPI.Read(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PassiveDiscoveryConfigServiceAPI.Read``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `Read`: ControllerReadPassiveDiscoveryConfigResponse
	fmt.Fprintf(os.Stdout, "Response from `PassiveDiscoveryConfigServiceAPI.Read`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | An application specific resource identity of a resource | 

### Other Parameters

Other parameters are passed through a pointer to a `PassiveDiscoveryConfigServiceAPIReadRequest` struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**fields** | **string** |   A collection of response resources can be transformed by specifying a set of JSON tags to be returned. For a â€œflatâ€ resource, the tag name is straightforward. If field selection is allowed on non-flat hierarchical resources, the service should implement a qualified naming scheme such as dot-qualification to reference data down the hierarchy. If a resource does not have the specified tag, the tag does not appear in the output resource.  Specify this parameter as a comma-separated list of JSON tag names.         | 

### Return type

[**ControllerReadPassiveDiscoveryConfigResponse**](ControllerReadPassiveDiscoveryConfigResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## Update

> ControllerUpdatePassiveDiscoveryConfigResponse Update(ctx, id).Body(body).Execute()

Update the PassiveDiscoveryConfig object. Use this method to update the PassiveDiscoveryConfig object.

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"

	"github.com/infobloxopen/universal-ddi-go-client/discoverycontroller"
)

func main() {
	id := "a5183192-1e00-475f-b334-38e1f0bb1bc7" // string | An application specific resource identity of a resource
	body := *discoverycontroller.NewControllerPassiveDiscoveryConfig() // ControllerPassiveDiscoveryConfig | 

	apiClient := discoverycontroller.NewAPIClient()
	resp, r, err := apiClient.PassiveDiscoveryConfigServiceAPI.Update(context.Background(), id).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PassiveDiscoveryConfigServiceAPI.Update``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `Update`: ControllerUpdatePassiveDiscoveryConfigResponse
	fmt.Fprintf(os.Stdout, "Response from `PassiveDiscoveryConfigServiceAPI.Update`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | An application specific resource identity of a resource | 

### Other Parameters

Other parameters are passed through a pointer to a `PassiveDiscoveryConfigServiceAPIUpdateRequest` struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**body** | [**ControllerPassiveDiscoveryConfig**](ControllerPassiveDiscoveryConfig.md) |  | 

### Return type

[**ControllerUpdatePassiveDiscoveryConfigResponse**](ControllerUpdatePassiveDiscoveryConfigResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

