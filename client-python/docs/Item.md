# Item

Represents a single document or data entry in the graph's Store. Items are used to store cross-thread memories.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace** | **List[str]** | The namespace of the item. A namespace is analogous to a document&#39;s directory. | 
**key** | **str** | The unique identifier of the item within its namespace. In general, keys needn&#39;t be globally unique. | 
**value** | **object** | The value stored in the item. This is the document itself. | 
**created_at** | **datetime** | The timestamp when the item was created. | 
**updated_at** | **datetime** | The timestamp when the item was last updated. | 

## Example

```python
from ap_client.models.item import Item

# TODO update the JSON string below
json = "{}"
# create an instance of Item from a JSON string
item_instance = Item.from_json(json)
# print the JSON string representation of the object
print(Item.to_json())

# convert the object into a dict
item_dict = item_instance.to_dict()
# create an instance of Item from a dict
item_from_dict = Item.from_dict(item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


