# RunCreate

Payload for creating a run.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**thread_id** | **str** | The ID of the thread to run. If not provided, will create a stateless run. | [optional] 
**agent_id** | **str** | The agent ID to run. If not provided will use the default agent for this service. | [optional] 
**input** | [**Input**](Input.md) |  | [optional] 
**messages** | [**List[Message]**](Message.md) | The messages to pass an input to the agent. | [optional] 
**metadata** | **object** | Metadata to assign to the run. | [optional] 
**config** | [**Config**](Config.md) |  | [optional] 
**webhook** | **str** | Webhook to call after run finishes. | [optional] 
**stream_mode** | [**StreamMode**](StreamMode.md) |  | [optional] 
**on_completion** | **str** | Whether to delete or keep the thread when run completes. Must be one of &#39;delete&#39; or &#39;keep&#39;. Defaults to &#39;delete&#39; when thread_id not provided, otherwise &#39;keep&#39;. | [optional] 
**on_disconnect** | **str** | The disconnect mode to use. Must be one of &#39;cancel&#39; or &#39;continue&#39;. | [optional] [default to 'cancel']
**if_not_exists** | **str** | How to handle missing thread. Must be either &#39;reject&#39; (raise error if missing), or &#39;create&#39; (create new thread). | [optional] [default to 'reject']

## Example

```python
from ap_client.models.run_create import RunCreate

# TODO update the JSON string below
json = "{}"
# create an instance of RunCreate from a JSON string
run_create_instance = RunCreate.from_json(json)
# print the JSON string representation of the object
print(RunCreate.to_json())

# convert the object into a dict
run_create_dict = run_create_instance.to_dict()
# create an instance of RunCreate from a dict
run_create_from_dict = RunCreate.from_dict(run_create_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


