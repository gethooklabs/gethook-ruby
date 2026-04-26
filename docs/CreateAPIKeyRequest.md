# Gethook::CreateAPIKeyRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **role** | **String** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::CreateAPIKeyRequest.new(
  name: My API Key,
  role: admin
)
```

