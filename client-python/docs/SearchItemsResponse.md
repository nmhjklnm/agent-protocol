# SearchItemsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Item]**](Item.md) |  | 

## Example

```python
from ap_client.models.search_items_response import SearchItemsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SearchItemsResponse from a JSON string
search_items_response_instance = SearchItemsResponse.from_json(json)
# print the JSON string representation of the object
print(SearchItemsResponse.to_json())

# convert the object into a dict
search_items_response_dict = search_items_response_instance.to_dict()
# create an instance of SearchItemsResponse from a dict
search_items_response_from_dict = SearchItemsResponse.from_dict(search_items_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


