# Gethook::PlatformStats

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_attempts** | **Integer** |  | [optional] |
| **events_delivered** | **Integer** |  | [optional] |
| **events_processed** | **Integer** |  | [optional] |
| **success_rate_pct** | **Float** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::PlatformStats.new(
  delivery_attempts: null,
  events_delivered: null,
  events_processed: null,
  success_rate_pct: null
)
```

