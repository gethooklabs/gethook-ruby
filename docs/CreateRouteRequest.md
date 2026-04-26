# Gethook::CreateRouteRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **destination_id** | **String** |  |  |
| **event_type_pattern** | **String** |  | [optional] |
| **source_id** | **String** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::CreateRouteRequest.new(
  destination_id: uuid,
  event_type_pattern: order.*,
  source_id: uuid
)
```

