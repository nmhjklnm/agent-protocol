# ThreadPatch

Payload for updating a thread.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checkpoint** | [**ThreadCheckpoint**](ThreadCheckpoint.md) | The identifier of the checkpoint to branch from. Ignored for metadata-only patches. If not provided, defaults to the latest checkpoint. | [optional] 
**metadata** | **object** | Metadata to merge with existing thread metadata. | [optional] 
**values** | **object** | Values to merge with existing thread values. | [optional] 
**messages** | [**List[Message]**](Message.md) | Messages to combine with current thread messages. | [optional] 

## Example

```python
from ap_client.models.thread_patch import ThreadPatch

# TODO update the JSON string below
json = "{}"
# create an instance of ThreadPatch from a JSON string
thread_patch_instance = ThreadPatch.from_json(json)
# print the JSON string representation of the object
print(ThreadPatch.to_json())

# convert the object into a dict
thread_patch_dict = thread_patch_instance.to_dict()
# create an instance of ThreadPatch from a dict
thread_patch_from_dict = ThreadPatch.from_dict(thread_patch_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


