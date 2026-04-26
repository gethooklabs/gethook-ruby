# Gethook::CreateSourceRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auth_mode** | **String** |  | [optional] |
| **name** | **String** |  |  |
| **verification_config** | **Object** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::CreateSourceRequest.new(
  auth_mode: none,
  name: Stripe webhooks,
  verification_config: null
)
```

