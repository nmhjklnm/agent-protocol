# ap_client.StoreApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_item**](StoreApi.md#delete_item) | **DELETE** /store/items | Delete Store Item
[**get_item**](StoreApi.md#get_item) | **GET** /store/items | Get Store Item
[**list_namespaces**](StoreApi.md#list_namespaces) | **POST** /store/namespaces | List namespaces
[**put_item**](StoreApi.md#put_item) | **PUT** /store/items | Insert or Update Item
[**search_items**](StoreApi.md#search_items) | **POST** /store/items/search | Search Store Items


# **delete_item**
> delete_item(store_delete_request)

Delete Store Item

### Example


```python
import ap_client
from ap_client.models.store_delete_request import StoreDeleteRequest
from ap_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = ap_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with ap_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ap_client.StoreApi(api_client)
    store_delete_request = ap_client.StoreDeleteRequest() # StoreDeleteRequest | 

    try:
        # Delete Store Item
        api_instance.delete_item(store_delete_request)
    except Exception as e:
        print("Exception when calling StoreApi->delete_item: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store_delete_request** | [**StoreDeleteRequest**](StoreDeleteRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Success |  -  |
**404** | Not Found |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_item**
> Item get_item(key, namespace=namespace)

Get Store Item

### Example


```python
import ap_client
from ap_client.models.item import Item
from ap_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = ap_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with ap_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ap_client.StoreApi(api_client)
    key = 'key_example' # str | 
    namespace = ['namespace_example'] # List[str] |  (optional)

    try:
        # Get Store Item
        api_response = api_instance.get_item(key, namespace=namespace)
        print("The response of StoreApi->get_item:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoreApi->get_item: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **str**|  | 
 **namespace** | [**List[str]**](str.md)|  | [optional] 

### Return type

[**Item**](Item.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**400** | Bad Request |  -  |
**404** | Not Found |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_namespaces**
> List[List[str]] list_namespaces(store_list_namespaces_request)

List namespaces

### Example


```python
import ap_client
from ap_client.models.store_list_namespaces_request import StoreListNamespacesRequest
from ap_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = ap_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with ap_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ap_client.StoreApi(api_client)
    store_list_namespaces_request = ap_client.StoreListNamespacesRequest() # StoreListNamespacesRequest | 

    try:
        # List namespaces
        api_response = api_instance.list_namespaces(store_list_namespaces_request)
        print("The response of StoreApi->list_namespaces:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoreApi->list_namespaces: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store_list_namespaces_request** | [**StoreListNamespacesRequest**](StoreListNamespacesRequest.md)|  | 

### Return type

**List[List[str]]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_item**
> put_item(store_put_request)

Insert or Update Item

### Example


```python
import ap_client
from ap_client.models.store_put_request import StorePutRequest
from ap_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = ap_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with ap_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ap_client.StoreApi(api_client)
    store_put_request = ap_client.StorePutRequest() # StorePutRequest | 

    try:
        # Insert or Update Item
        api_instance.put_item(store_put_request)
    except Exception as e:
        print("Exception when calling StoreApi->put_item: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store_put_request** | [**StorePutRequest**](StorePutRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Success |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **search_items**
> SearchItemsResponse search_items(store_search_request)

Search Store Items

### Example


```python
import ap_client
from ap_client.models.search_items_response import SearchItemsResponse
from ap_client.models.store_search_request import StoreSearchRequest
from ap_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = ap_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with ap_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ap_client.StoreApi(api_client)
    store_search_request = ap_client.StoreSearchRequest() # StoreSearchRequest | 

    try:
        # Search Store Items
        api_response = api_instance.search_items(store_search_request)
        print("The response of StoreApi->search_items:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoreApi->search_items: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store_search_request** | [**StoreSearchRequest**](StoreSearchRequest.md)|  | 

### Return type

[**SearchItemsResponse**](SearchItemsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

