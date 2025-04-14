# Run


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**run_id** | **str** | The ID of the run. | 
**thread_id** | **str** | The ID of the thread. | 
**agent_id** | **str** | The agent that was used for this run. | [optional] 
**created_at** | **datetime** | The time the run was created. | 
**updated_at** | **datetime** | The last time the run was updated. | 
**status** | [**RunStatus**](RunStatus.md) | The status of the run. | 
**metadata** | **object** | The run metadata. | 
**kwargs** | **object** |  | 
**multitask_strategy** | **str** | Strategy to handle concurrent runs on the same thread. | 

## Example

```python
from ap_client.models.run import Run

# TODO update the JSON string below
json = "{}"
# create an instance of Run from a JSON string
run_instance = Run.from_json(json)
# print the JSON string representation of the object
print(Run.to_json())

# convert the object into a dict
run_dict = run_instance.to_dict()
# create an instance of Run from a dict
run_from_dict = Run.from_dict(run_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


