# Gethook::Route

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **active** | **Boolean** |  |  |
| **created_at** | **String** |  |  |
| **destination_id** | **String** |  |  |
| **event_type_pattern** | **String** |  | [optional] |
| **id** | **String** |  |  |
| **retry_policy** | **Object** |  |  |
| **source_id** | **String** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::Route.new(
  account_id: null,
  active: null,
  created_at: null,
  destination_id: null,
  event_type_pattern: null,
  id: null,
  retry_policy: null,
  source_id: null
)
```

