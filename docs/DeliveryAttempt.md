# Gethook::DeliveryAttempt

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attempt_number** | **Integer** |  |  |
| **destination_id** | **String** |  |  |
| **error_message** | **String** |  | [optional] |
| **event_id** | **String** |  |  |
| **finished_at** | **String** |  | [optional] |
| **id** | **String** |  |  |
| **latency_ms** | **Integer** |  | [optional] |
| **outcome** | [**AttemptOutcome**](AttemptOutcome.md) |  |  |
| **response_body** | **String** |  | [optional] |
| **response_status** | **Integer** |  | [optional] |
| **started_at** | **String** |  |  |

## Example

```ruby
require 'gethook'

instance = Gethook::DeliveryAttempt.new(
  attempt_number: null,
  destination_id: null,
  error_message: null,
  event_id: null,
  finished_at: null,
  id: null,
  latency_ms: null,
  outcome: null,
  response_body: null,
  response_status: null,
  started_at: null
)
```

