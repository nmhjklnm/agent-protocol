# StorePutRequest

Request to store or update an item.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace** | **List[str]** | A list of strings representing the namespace path. | 
**key** | **str** | The unique identifier for the item within the namespace. | 
**value** | **object** | A dictionary containing the item&#39;s data. | 

## Example

```python
from ap_client.models.store_put_request import StorePutRequest

# TODO update the JSON string below
json = "{}"
# create an instance of StorePutRequest from a JSON string
store_put_request_instance = StorePutRequest.from_json(json)
# print the JSON string representation of the object
print(StorePutRequest.to_json())

# convert the object into a dict
store_put_request_dict = store_put_request_instance.to_dict()
# create an instance of StorePutRequest from a dict
store_put_request_from_dict = StorePutRequest.from_dict(store_put_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


