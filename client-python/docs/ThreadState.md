# ThreadState


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checkpoint** | [**ThreadCheckpoint**](ThreadCheckpoint.md) | The identifier for this checkpoint. | 
**values** | **object** | The current state of the thread. | 
**messages** | [**List[Message]**](Message.md) | The current messages of the thread. If messages are contained in Thread.values, implementations should remove them from values when returning messages. When this key isn&#39;t present it means the thread/agent doesn&#39;t support messages. | [optional] 
**metadata** | **object** | The checkpoint metadata. | [optional] 

## Example

```python
from ap_client.models.thread_state import ThreadState

# TODO update the JSON string below
json = "{}"
# create an instance of ThreadState from a JSON string
thread_state_instance = ThreadState.from_json(json)
# print the JSON string representation of the object
print(ThreadState.to_json())

# convert the object into a dict
thread_state_dict = thread_state_instance.to_dict()
# create an instance of ThreadState from a dict
thread_state_from_dict = ThreadState.from_dict(thread_state_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


