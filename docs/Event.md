# Gethook::Event

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **attempts_count** | **Integer** |  |  |
| **body** | **String** |  |  |
| **created_at** | **String** |  |  |
| **created_by** | **String** |  | [optional] |
| **direction** | [**Direction**](Direction.md) |  |  |
| **event_type** | **String** |  | [optional] |
| **external_event_id** | **String** |  | [optional] |
| **final_state** | **String** |  | [optional] |
| **headers** | **Hash&lt;String, Object&gt;** |  |  |
| **id** | **String** |  |  |
| **next_attempt_at** | **String** |  | [optional] |
| **payload_hash** | **String** |  | [optional] |
| **received_at** | **String** |  |  |
| **source_id** | **String** |  | [optional] |
| **status** | [**EventStatus**](EventStatus.md) |  |  |

## Example

```ruby
require 'gethook'

instance = Gethook::Event.new(
  account_id: null,
  attempts_count: null,
  body: null,
  created_at: null,
  created_by: null,
  direction: null,
  event_type: null,
  external_event_id: null,
  final_state: null,
  headers: null,
  id: null,
  next_attempt_at: null,
  payload_hash: null,
  received_at: null,
  source_id: null,
  status: null
)
```

