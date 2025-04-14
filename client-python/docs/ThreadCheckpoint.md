# ThreadCheckpoint

Structured identifier for a thread checkpoint, ie. an entry in the thread's history.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checkpoint_id** | **str** | The ID of the checkpoint. | 

## Example

```python
from ap_client.models.thread_checkpoint import ThreadCheckpoint

# TODO update the JSON string below
json = "{}"
# create an instance of ThreadCheckpoint from a JSON string
thread_checkpoint_instance = ThreadCheckpoint.from_json(json)
# print the JSON string representation of the object
print(ThreadCheckpoint.to_json())

# convert the object into a dict
thread_checkpoint_dict = thread_checkpoint_instance.to_dict()
# create an instance of ThreadCheckpoint from a dict
thread_checkpoint_from_dict = ThreadCheckpoint.from_dict(thread_checkpoint_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


