# MessageTextBlock


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**type** | **object** |  | 
**metadata** | **object** |  | [optional] 

## Example

```python
from ap_client.models.message_text_block import MessageTextBlock

# TODO update the JSON string below
json = "{}"
# create an instance of MessageTextBlock from a JSON string
message_text_block_instance = MessageTextBlock.from_json(json)
# print the JSON string representation of the object
print(MessageTextBlock.to_json())

# convert the object into a dict
message_text_block_dict = message_text_block_instance.to_dict()
# create an instance of MessageTextBlock from a dict
message_text_block_from_dict = MessageTextBlock.from_dict(message_text_block_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


