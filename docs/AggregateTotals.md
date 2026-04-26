# Gethook::AggregateTotals

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **Integer** |  |  |
| **delivered** | **Integer** |  |  |
| **failed** | **Integer** |  |  |

## Example

```ruby
require 'gethook'

instance = Gethook::AggregateTotals.new(
  total: 1500,
  delivered: 1420,
  failed: 12
)
```

