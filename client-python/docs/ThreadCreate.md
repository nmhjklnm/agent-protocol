# ThreadCreate

Payload for creating a thread.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**thread_id** | **str** | The ID of the thread. If not provided, a random UUID will be generated. | [optional] 
**metadata** | **object** | Metadata to add to thread. | [optional] 
**if_exists** | **str** | How to handle duplicate creation. Must be either &#39;raise&#39; (raise error if duplicate), or &#39;do_nothing&#39; (return existing thread). | [optional] [default to 'raise']

## Example

```python
from ap_client.models.thread_create import ThreadCreate

# TODO update the JSON string below
json = "{}"
# create an instance of ThreadCreate from a JSON string
thread_create_instance = ThreadCreate.from_json(json)
# print the JSON string representation of the object
print(ThreadCreate.to_json())

# convert the object into a dict
thread_create_dict = thread_create_instance.to_dict()
# create an instance of ThreadCreate from a dict
thread_create_from_dict = ThreadCreate.from_dict(thread_create_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


