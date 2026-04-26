# Gethook::StatsData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **by_status** | [**Array&lt;StatsStatusItem&gt;**](StatsStatusItem.md) |  |  |
| **daily** | [**Array&lt;StatsDailyItem&gt;**](StatsDailyItem.md) |  |  |
| **totals** | [**AggregateTotals**](AggregateTotals.md) |  |  |

## Example

```ruby
require 'gethook'

instance = Gethook::StatsData.new(
  by_status: null,
  daily: null,
  totals: null
)
```

