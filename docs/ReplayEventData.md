# Gethook::ReplayEventData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **original_event_id** | **String** |  |  |
| **replay_event_id** | **String** |  |  |
| **status** | **String** |  |  |

## Example

```ruby
require 'gethook'

instance = Gethook::ReplayEventData.new(
  original_event_id: uuid,
  replay_event_id: uuid,
  status: queued
)
```

