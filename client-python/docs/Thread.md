# Thread


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**thread_id** | **str** | The ID of the thread. | 
**created_at** | **datetime** | The time the thread was created. | 
**updated_at** | **datetime** | The last time the thread was updated. | 
**metadata** | **object** | The thread metadata. | 
**status** | [**ThreadStatus**](ThreadStatus.md) | The status of the thread. | 
**values** | **object** | The current state of the thread. | [optional] 
**messages** | [**List[Message]**](Message.md) | The current Messages of the thread. If messages are contained in Thread.values, implementations should remove them from values when returning messages. When this key isn&#39;t present it means the thread/agent doesn&#39;t support messages. | [optional] 

## Example

```python
from ap_client.models.thread import Thread

# TODO update the JSON string below
json = "{}"
# create an instance of Thread from a JSON string
thread_instance = Thread.from_json(json)
# print the JSON string representation of the object
print(Thread.to_json())

# convert the object into a dict
thread_dict = thread_instance.to_dict()
# create an instance of Thread from a dict
thread_from_dict = Thread.from_dict(thread_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


