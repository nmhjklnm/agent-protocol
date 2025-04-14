# ThreadSearchRequest

Payload for listing threads.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metadata** | **object** | Thread metadata to filter on. | [optional] 
**values** | **object** | State values to filter on. | [optional] 
**status** | [**ThreadStatus**](ThreadStatus.md) | Thread status to filter on. | [optional] 
**limit** | **int** | Maximum number to return. | [optional] [default to 10]
**offset** | **int** | Offset to start from. | [optional] [default to 0]

## Example

```python
from ap_client.models.thread_search_request import ThreadSearchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ThreadSearchRequest from a JSON string
thread_search_request_instance = ThreadSearchRequest.from_json(json)
# print the JSON string representation of the object
print(ThreadSearchRequest.to_json())

# convert the object into a dict
thread_search_request_dict = thread_search_request_instance.to_dict()
# create an instance of ThreadSearchRequest from a dict
thread_search_request_from_dict = ThreadSearchRequest.from_dict(thread_search_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


