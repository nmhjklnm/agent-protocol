# StoreListNamespacesRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prefix** | **List[str]** | Optional list of strings representing the prefix to filter namespaces. | [optional] 
**suffix** | **List[str]** | Optional list of strings representing the suffix to filter namespaces. | [optional] 
**max_depth** | **int** | Optional integer specifying the maximum depth of namespaces to return. | [optional] 
**limit** | **int** | Maximum number of namespaces to return (default is 100). | [optional] [default to 100]
**offset** | **int** | Number of namespaces to skip before returning results (default is 0). | [optional] [default to 0]

## Example

```python
from ap_client.models.store_list_namespaces_request import StoreListNamespacesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of StoreListNamespacesRequest from a JSON string
store_list_namespaces_request_instance = StoreListNamespacesRequest.from_json(json)
# print the JSON string representation of the object
print(StoreListNamespacesRequest.to_json())

# convert the object into a dict
store_list_namespaces_request_dict = store_list_namespaces_request_instance.to_dict()
# create an instance of StoreListNamespacesRequest from a dict
store_list_namespaces_request_from_dict = StoreListNamespacesRequest.from_dict(store_list_namespaces_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


