# AgentCapabilities

Describes which protocol features the agent supports. In addition to the standard capabilities (prefixed with ap.), implementations can declare custom capabilities, named in reverse domain notation (eg. com.example.some.capability).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ap_io_messages** | **bool** | Whether the agent supports Messages as input/output/state. If true, the agent uses the &#x60;messages&#x60; key in threads/runs endpoints. | [optional] 
**ap_io_streaming** | **bool** | Whether the agent supports streaming output. | [optional] 

## Example

```python
from ap_client.models.agent_capabilities import AgentCapabilities

# TODO update the JSON string below
json = "{}"
# create an instance of AgentCapabilities from a JSON string
agent_capabilities_instance = AgentCapabilities.from_json(json)
# print the JSON string representation of the object
print(AgentCapabilities.to_json())

# convert the object into a dict
agent_capabilities_dict = agent_capabilities_instance.to_dict()
# create an instance of AgentCapabilities from a dict
agent_capabilities_from_dict = AgentCapabilities.from_dict(agent_capabilities_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


