# RunWaitResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**run** | [**Run**](Run.md) | The run information. | [optional] 
**values** | **object** | The values returned by the run. | [optional] 
**messages** | [**List[Message]**](Message.md) | The messages returned by the run. | [optional] 

## Example

```python
from ap_client.models.run_wait_response import RunWaitResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RunWaitResponse from a JSON string
run_wait_response_instance = RunWaitResponse.from_json(json)
# print the JSON string representation of the object
print(RunWaitResponse.to_json())

# convert the object into a dict
run_wait_response_dict = run_wait_response_instance.to_dict()
# create an instance of RunWaitResponse from a dict
run_wait_response_from_dict = RunWaitResponse.from_dict(run_wait_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


