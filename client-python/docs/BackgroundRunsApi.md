# ap_client.BackgroundRunsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_run**](BackgroundRunsApi.md#cancel_run) | **POST** /runs/{run_id}/cancel | Cancel Run
[**create_run**](BackgroundRunsApi.md#create_run) | **POST** /runs | Create Background Run
[**delete_run**](BackgroundRunsApi.md#delete_run) | **DELETE** /runs/{run_id} | Delete Run
[**get_run**](BackgroundRunsApi.md#get_run) | **GET** /runs/{run_id} | Get Run
[**search_thread_runs**](BackgroundRunsApi.md#search_thread_runs) | **GET** /threads/{thread_id}/runs | Search Thread Runs
[**stream_run**](BackgroundRunsApi.md#stream_run) | **GET** /runs/{run_id}/stream | Stream output from Run
[**wait_run**](BackgroundRunsApi.md#wait_run) | **GET** /runs/{run_id}/wait | Wait for Run output


# **cancel_run**
> cancel_run(run_id, wait=wait, action=action)

Cancel Run

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
    api_instance = ap_client.BackgroundRunsApi(api_client)
    run_id = 'run_id_example' # str | The ID of the run.
    wait = False # bool |  (optional) (default to False)
    action = interrupt # str | Action to take when cancelling the run. Possible values are `interrupt` or `rollback`. `interrupt` will simply cancel the run. `rollback` will cancel the run and delete the run and associated checkpoints afterwards. (optional) (default to interrupt)

    try:
        # Cancel Run
        api_instance.cancel_run(run_id, wait=wait, action=action)
    except Exception as e:
        print("Exception when calling BackgroundRunsApi->cancel_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **run_id** | **str**| The ID of the run. | 
 **wait** | **bool**|  | [optional] [default to False]
 **action** | **str**| Action to take when cancelling the run. Possible values are &#x60;interrupt&#x60; or &#x60;rollback&#x60;. &#x60;interrupt&#x60; will simply cancel the run. &#x60;rollback&#x60; will cancel the run and delete the run and associated checkpoints afterwards. | [optional] [default to interrupt]

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

# **create_run**
> object create_run(run_create)

Create Background Run

Create a run in a new thread, return the run ID immediately. Don't wait for the final run output.

### Example


```python
import ap_client
from ap_client.models.run_create import RunCreate
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
    api_instance = ap_client.BackgroundRunsApi(api_client)
    run_create = ap_client.RunCreate() # RunCreate | 

    try:
        # Create Background Run
        api_response = api_instance.create_run(run_create)
        print("The response of BackgroundRunsApi->create_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackgroundRunsApi->create_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **run_create** | [**RunCreate**](RunCreate.md)|  | 

### Return type

**object**

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
**409** | Conflict |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_run**
> delete_run(run_id)

Delete Run

Delete a run by ID.

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
    api_instance = ap_client.BackgroundRunsApi(api_client)
    run_id = 'run_id_example' # str | The ID of the run.

    try:
        # Delete Run
        api_instance.delete_run(run_id)
    except Exception as e:
        print("Exception when calling BackgroundRunsApi->delete_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **run_id** | **str**| The ID of the run. | 

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

# **get_run**
> Run get_run(run_id)

Get Run

Get a run by ID.

### Example


```python
import ap_client
from ap_client.models.run import Run
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
    api_instance = ap_client.BackgroundRunsApi(api_client)
    run_id = 'run_id_example' # str | The ID of the run.

    try:
        # Get Run
        api_response = api_instance.get_run(run_id)
        print("The response of BackgroundRunsApi->get_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackgroundRunsApi->get_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **run_id** | **str**| The ID of the run. | 

### Return type

[**Run**](Run.md)

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

# **search_thread_runs**
> List[Run] search_thread_runs(thread_id, limit=limit, offset=offset)

Search Thread Runs

List runs for a thread.

### Example


```python
import ap_client
from ap_client.models.run import Run
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
    api_instance = ap_client.BackgroundRunsApi(api_client)
    thread_id = 'thread_id_example' # str | The ID of the thread.
    limit = 10 # int |  (optional) (default to 10)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # Search Thread Runs
        api_response = api_instance.search_thread_runs(thread_id, limit=limit, offset=offset)
        print("The response of BackgroundRunsApi->search_thread_runs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackgroundRunsApi->search_thread_runs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **thread_id** | **str**| The ID of the thread. | 
 **limit** | **int**|  | [optional] [default to 10]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**List[Run]**](Run.md)

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

# **stream_run**
> object stream_run(run_id)

Stream output from Run

Join the output stream of an existing run. This endpoint streams output in real-time from a run similar to the /threads/__THREAD_ID__/runs/stream endpoint. Only output produced after this endpoint is called will be streamed.

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
    api_instance = ap_client.BackgroundRunsApi(api_client)
    run_id = 'run_id_example' # str | The ID of the run.

    try:
        # Stream output from Run
        api_response = api_instance.stream_run(run_id)
        print("The response of BackgroundRunsApi->stream_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackgroundRunsApi->stream_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **run_id** | **str**| The ID of the run. | 

### Return type

**object**

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

# **wait_run**
> RunWaitResponse wait_run(run_id)

Wait for Run output

Wait for a run to finish, return the final output. If the run already finished, returns its final output immediately.

### Example


```python
import ap_client
from ap_client.models.run_wait_response import RunWaitResponse
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
    api_instance = ap_client.BackgroundRunsApi(api_client)
    run_id = 'run_id_example' # str | The ID of the run.

    try:
        # Wait for Run output
        api_response = api_instance.wait_run(run_id)
        print("The response of BackgroundRunsApi->wait_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackgroundRunsApi->wait_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **run_id** | **str**| The ID of the run. | 

### Return type

[**RunWaitResponse**](RunWaitResponse.md)

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

