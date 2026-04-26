# Gethook::StatsDailyItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date** | **String** |  |  |
| **delivered** | **Integer** |  |  |
| **failed** | **Integer** |  |  |
| **inbound** | **Integer** |  |  |
| **outbound** | **Integer** |  |  |

## Example

```ruby
require 'gethook'

instance = Gethook::StatsDailyItem.new(
  date: 2024-01-15,
  delivered: 35,
  failed: 3,
  inbound: 42,
  outbound: 38
)
```

