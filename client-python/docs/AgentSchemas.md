# AgentSchemas

Defines the structure and properties of an agent.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agent_id** | **str** | The ID of the agent. | 
**input_schema** | **object** | The schema for the agent input. In JSON Schema format. | 
**output_schema** | **object** | The schema for the agent output. In JSON Schema format. | 
**state_schema** | **object** | The schema for the agent&#39;s internal state. In JSON Schema format. | [optional] 
**config_schema** | **object** | The schema for the agent config. In JSON Schema format. | [optional] 

## Example

```python
from ap_client.models.agent_schemas import AgentSchemas

# TODO update the JSON string below
json = "{}"
# create an instance of AgentSchemas from a JSON string
agent_schemas_instance = AgentSchemas.from_json(json)
# print the JSON string representation of the object
print(AgentSchemas.to_json())

# convert the object into a dict
agent_schemas_dict = agent_schemas_instance.to_dict()
# create an instance of AgentSchemas from a dict
agent_schemas_from_dict = AgentSchemas.from_dict(agent_schemas_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


