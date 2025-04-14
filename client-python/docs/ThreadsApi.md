# ap_client.ThreadsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**copy_thread**](ThreadsApi.md#copy_thread) | **POST** /threads/{thread_id}/copy | Copy Thread
[**create_thread**](ThreadsApi.md#create_thread) | **POST** /threads | Create Thread
[**delete_thread**](ThreadsApi.md#delete_thread) | **DELETE** /threads/{thread_id} | Delete Thread
[**get_thread**](ThreadsApi.md#get_thread) | **GET** /threads/{thread_id} | Get Thread
[**get_thread_history**](ThreadsApi.md#get_thread_history) | **GET** /threads/{thread_id}/history | Get Thread History
[**patch_thread**](ThreadsApi.md#patch_thread) | **PATCH** /threads/{thread_id} | Patch Thread
[**search_threads**](ThreadsApi.md#search_threads) | **POST** /threads/search | Search Threads


# **copy_thread**
> Thread copy_thread(thread_id)

Copy Thread

Create a new thread with a copy of the state and checkpoints from an existing thread.

### Example


```python
import ap_client
from ap_client.models.thread import Thread
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
    api_instance = ap_client.ThreadsApi(api_client)
    thread_id = 'thread_id_example' # str | The ID of the thread.

    try:
        # Copy Thread
        api_response = api_instance.copy_thread(thread_id)
        print("The response of ThreadsApi->copy_thread:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ThreadsApi->copy_thread: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **thread_id** | **str**| The ID of the thread. | 

### Return type

[**Thread**](Thread.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**404** | Not Found |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_thread**
> Thread create_thread(thread_create)

Create Thread

Create a thread.

### Example


```python
import ap_client
from ap_client.models.thread import Thread
from ap_client.models.thread_create import ThreadCreate
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
    api_instance = ap_client.ThreadsApi(api_client)
    thread_create = ap_client.ThreadCreate() # ThreadCreate | 

    try:
        # Create Thread
        api_response = api_instance.create_thread(thread_create)
        print("The response of ThreadsApi->create_thread:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ThreadsApi->create_thread: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **thread_create** | [**ThreadCreate**](ThreadCreate.md)|  | 

### Return type

[**Thread**](Thread.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**409** | Conflict |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_thread**
> delete_thread(thread_id)

Delete Thread

Delete a thread by ID.

### Example


```python
import ap_client
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
    api_instance = ap_client.ThreadsApi(api_client)
    thread_id = 'thread_id_example' # str | The ID of the thread.

    try:
        # Delete Thread
        api_instance.delete_thread(thread_id)
    except Exception as e:
        print("Exception when calling ThreadsApi->delete_thread: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **thread_id** | **str**| The ID of the thread. | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Success |  -  |
**404** | Not Found |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_thread**
> Thread get_thread(thread_id)

Get Thread

Get a thread by ID.

### Example


```python
import ap_client
from ap_client.models.thread import Thread
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
    api_instance = ap_client.ThreadsApi(api_client)
    thread_id = 'thread_id_example' # str | The ID of the thread.

    try:
        # Get Thread
        api_response = api_instance.get_thread(thread_id)
        print("The response of ThreadsApi->get_thread:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ThreadsApi->get_thread: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **thread_id** | **str**| The ID of the thread. | 

### Return type

[**Thread**](Thread.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**404** | Not Found |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_thread_history**
> List[ThreadState] get_thread_history(thread_id, limit=limit, before=before)

Get Thread History

Get all past states for a thread.

### Example


```python
import ap_client
from ap_client.models.thread_state import ThreadState
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
    api_instance = ap_client.ThreadsApi(api_client)
    thread_id = 'thread_id_example' # str | The ID of the thread.
    limit = 10 # int |  (optional) (default to 10)
    before = 'before_example' # str |  (optional)

    try:
        # Get Thread History
        api_response = api_instance.get_thread_history(thread_id, limit=limit, before=before)
        print("The response of ThreadsApi->get_thread_history:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ThreadsApi->get_thread_history: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **thread_id** | **str**| The ID of the thread. | 
 **limit** | **int**|  | [optional] [default to 10]
 **before** | **str**|  | [optional] 

### Return type

[**List[ThreadState]**](ThreadState.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**404** | Not Found |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_thread**
> Thread patch_thread(thread_id, thread_patch)

Patch Thread

Update a thread.

### Example


```python
import ap_client
from ap_client.models.thread import Thread
from ap_client.models.thread_patch import ThreadPatch
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
    api_instance = ap_client.ThreadsApi(api_client)
    thread_id = 'thread_id_example' # str | The ID of the thread.
    thread_patch = ap_client.ThreadPatch() # ThreadPatch | 

    try:
        # Patch Thread
        api_response = api_instance.patch_thread(thread_id, thread_patch)
        print("The response of ThreadsApi->patch_thread:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ThreadsApi->patch_thread: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **thread_id** | **str**| The ID of the thread. | 
 **thread_patch** | [**ThreadPatch**](ThreadPatch.md)|  | 

### Return type

[**Thread**](Thread.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**404** | Not Found |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **search_threads**
> List[Thread] search_threads(thread_search_request)

Search Threads

Search for threads.

This endpoint also functions as the endpoint to list all threads.

### Example


```python
import ap_client
from ap_client.models.thread import Thread
from ap_client.models.thread_search_request import ThreadSearchRequest
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
    api_instance = ap_client.ThreadsApi(api_client)
    thread_search_request = ap_client.ThreadSearchRequest() # ThreadSearchRequest | 

    try:
        # Search Threads
        api_response = api_instance.search_threads(thread_search_request)
        print("The response of ThreadsApi->search_threads:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ThreadsApi->search_threads: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **thread_search_request** | [**ThreadSearchRequest**](ThreadSearchRequest.md)|  | 

### Return type

[**List[Thread]**](Thread.md)

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

