# Gethook::CreateCustomDomainRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **domain** | **String** |  |  |
| **type** | **String** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::CreateCustomDomainRequest.new(
  domain: webhooks.example.com,
  type: webhook
)
```

