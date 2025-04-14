# StoreDeleteRequest

Request to delete an item.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace** | **List[str]** | A list of strings representing the namespace path. | [optional] 
**key** | **str** | The unique identifier for the item. | 

## Example

```python
from ap_client.models.store_delete_request import StoreDeleteRequest

# TODO update the JSON string below
json = "{}"
# create an instance of StoreDeleteRequest from a JSON string
store_delete_request_instance = StoreDeleteRequest.from_json(json)
# print the JSON string representation of the object
print(StoreDeleteRequest.to_json())

# convert the object into a dict
store_delete_request_dict = store_delete_request_instance.to_dict()
# create an instance of StoreDeleteRequest from a dict
store_delete_request_from_dict = StoreDeleteRequest.from_dict(store_delete_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


