# Gethook::RegisterRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **email** | **String** |  |  |
| **password** | **String** |  |  |

## Example

```ruby
require 'gethook'

instance = Gethook::RegisterRequest.new(
  name: Acme Corp,
  email: user@example.com,
  password: s3cr3t123
)
```

