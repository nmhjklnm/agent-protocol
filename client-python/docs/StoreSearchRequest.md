# StoreSearchRequest

Request to search for items

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace_prefix** | **List[str]** | List of strings representing the namespace prefix. | [optional] 
**filter** | **Dict[str, object]** | Optional dictionary of key-value pairs to filter results. | [optional] 
**limit** | **int** | Maximum number of items to return (default is 10). | [optional] [default to 10]
**offset** | **int** | Number of items to skip before returning results (default is 0). | [optional] [default to 0]

## Example

```python
from ap_client.models.store_search_request import StoreSearchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of StoreSearchRequest from a JSON string
store_search_request_instance = StoreSearchRequest.from_json(json)
# print the JSON string representation of the object
print(StoreSearchRequest.to_json())

# convert the object into a dict
store_search_request_dict = store_search_request_instance.to_dict()
# create an instance of StoreSearchRequest from a dict
store_search_request_from_dict = StoreSearchRequest.from_dict(store_search_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


