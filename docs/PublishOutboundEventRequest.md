# Gethook::PublishOutboundEventRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event_type** | **String** |  | [optional] |
| **external_event_id** | **String** |  | [optional] |
| **payload** | **String** |  |  |

## Example

```ruby
require 'gethook'

instance = Gethook::PublishOutboundEventRequest.new(
  event_type: order.created,
  external_event_id: evt_abc123,
  payload: {&quot;order_id&quot;:&quot;123&quot;}
)
```

