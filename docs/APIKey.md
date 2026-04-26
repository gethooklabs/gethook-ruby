# Gethook::APIKey

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **account_id** | **String** |  |  |
| **user_id** | **String** |  | [optional] |
| **name** | **String** |  |  |
| **role** | **String** |  |  |
| **key_prefix** | **String** |  |  |
| **created_at** | **String** |  |  |
| **revoked_at** | **String** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::APIKey.new(
  id: null,
  account_id: null,
  user_id: null,
  name: null,
  role: null,
  key_prefix: null,
  created_at: null,
  revoked_at: null
)
```

