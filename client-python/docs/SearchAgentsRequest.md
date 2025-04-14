# SearchAgentsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Name of the agent to search. | [optional] 
**metadata** | **object** | Metadata of the agent to search. | [optional] 
**limit** | **int** | Maximum number to return. | [optional] [default to 10]
**offset** | **int** | Offset to start from. | [optional] [default to 0]

## Example

```python
from ap_client.models.search_agents_request import SearchAgentsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SearchAgentsRequest from a JSON string
search_agents_request_instance = SearchAgentsRequest.from_json(json)
# print the JSON string representation of the object
print(SearchAgentsRequest.to_json())

# convert the object into a dict
search_agents_request_dict = search_agents_request_instance.to_dict()
# create an instance of SearchAgentsRequest from a dict
search_agents_request_from_dict = SearchAgentsRequest.from_dict(search_agents_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


