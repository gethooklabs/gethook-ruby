# Gethook::RetryPolicy

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **max_attempts** | **Integer** |  | [optional] |
| **backoff** | **String** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::RetryPolicy.new(
  max_attempts: null,
  backoff: null
)
```

