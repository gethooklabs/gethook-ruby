# Gethook::CreateDestinationRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auth_config** | **Object** |  | [optional] |
| **custom_headers** | **Object** |  | [optional] |
| **name** | **String** |  |  |
| **signing_secret** | **String** |  | [optional] |
| **timeout_seconds** | **Integer** |  | [optional] |
| **url** | **String** |  |  |

## Example

```ruby
require 'gethook'

instance = Gethook::CreateDestinationRequest.new(
  auth_config: null,
  custom_headers: null,
  name: My endpoint,
  signing_secret: my-secret,
  timeout_seconds: 30,
  url: https://example.com/webhooks
)
```

