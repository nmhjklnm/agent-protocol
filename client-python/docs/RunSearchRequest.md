# RunSearchRequest

Payload for listing runs.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metadata** | **object** | Run metadata to filter on. | [optional] 
**status** | [**RunStatus**](RunStatus.md) | Run status to filter on. | [optional] 
**thread_id** | **str** | The ID of the thread to filter on. | [optional] 
**agent_id** | **str** | The ID of the agent to filter on. | [optional] 
**limit** | **int** | Maximum number to return. | [optional] [default to 10]
**offset** | **int** | Offset to start from. | [optional] [default to 0]

## Example

```python
from ap_client.models.run_search_request import RunSearchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RunSearchRequest from a JSON string
run_search_request_instance = RunSearchRequest.from_json(json)
# print the JSON string representation of the object
print(RunSearchRequest.to_json())

# convert the object into a dict
run_search_request_dict = run_search_request_instance.to_dict()
# create an instance of RunSearchRequest from a dict
run_search_request_from_dict = RunSearchRequest.from_dict(run_search_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


