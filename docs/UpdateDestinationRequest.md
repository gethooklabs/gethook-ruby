# Gethook::UpdateDestinationRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **active** | **Boolean** |  | [optional] |
| **auth_config** | **Object** |  | [optional] |
| **custom_headers** | **Object** |  | [optional] |
| **name** | **String** |  | [optional] |
| **timeout_seconds** | **Integer** |  | [optional] |
| **url** | **String** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::UpdateDestinationRequest.new(
  active: true,
  auth_config: null,
  custom_headers: null,
  name: Updated name,
  timeout_seconds: 60,
  url: https://example.com/new
)
```

