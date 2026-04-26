# Gethook::OutboundEventsApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_outbound_event**](OutboundEventsApi.md#get_outbound_event) | **GET** /v1/outbound-events/{id} | Get outbound event |
| [**list_outbound_events**](OutboundEventsApi.md#list_outbound_events) | **GET** /v1/outbound-events | List outbound events |
| [**publish_outbound_event**](OutboundEventsApi.md#publish_outbound_event) | **POST** /v1/outbound-events | Publish outbound event |
| [**replay_outbound_event**](OutboundEventsApi.md#replay_outbound_event) | **POST** /v1/outbound-events/{id}/replay | Replay outbound event |


## get_outbound_event

> <EventDetailData> get_outbound_event(id)

Get outbound event

### Examples

```ruby
require 'time'
require 'gethook'
# setup authorization
Gethook.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['Authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['Authorization'] = 'Bearer'
end

api_instance = Gethook::OutboundEventsApi.new
id = 'id_example' # String | Event UUID

begin
  # Get outbound event
  result = api_instance.get_outbound_event(id)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling OutboundEventsApi->get_outbound_event: #{e}"
end
```

#### Using the get_outbound_event_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EventDetailData>, Integer, Hash)> get_outbound_event_with_http_info(id)

```ruby
begin
  # Get outbound event
  data, status_code, headers = api_instance.get_outbound_event_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EventDetailData>
rescue Gethook::ApiError => e
  puts "Error when calling OutboundEventsApi->get_outbound_event_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Event UUID |  |

### Return type

[**EventDetailData**](EventDetailData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_outbound_events

> <EventListData> list_outbound_events(opts)

List outbound events

### Examples

```ruby
require 'time'
require 'gethook'
# setup authorization
Gethook.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['Authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['Authorization'] = 'Bearer'
end

api_instance = Gethook::OutboundEventsApi.new
opts = {
  limit: 56, # Integer | Max results (default 25, max 200)
  offset: 56 # Integer | Pagination offset
}

begin
  # List outbound events
  result = api_instance.list_outbound_events(opts)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling OutboundEventsApi->list_outbound_events: #{e}"
end
```

#### Using the list_outbound_events_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EventListData>, Integer, Hash)> list_outbound_events_with_http_info(opts)

```ruby
begin
  # List outbound events
  data, status_code, headers = api_instance.list_outbound_events_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EventListData>
rescue Gethook::ApiError => e
  puts "Error when calling OutboundEventsApi->list_outbound_events_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** | Max results (default 25, max 200) | [optional] |
| **offset** | **Integer** | Pagination offset | [optional] |

### Return type

[**EventListData**](EventListData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## publish_outbound_event

> <PublishOutboundData> publish_outbound_event(publish_outbound_event_request)

Publish outbound event

Queues a new outbound event for delivery to all matching route destinations.

### Examples

```ruby
require 'time'
require 'gethook'
# setup authorization
Gethook.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['Authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['Authorization'] = 'Bearer'
end

api_instance = Gethook::OutboundEventsApi.new
publish_outbound_event_request = Gethook::PublishOutboundEventRequest.new({payload: '{"order_id":"123"}'}) # PublishOutboundEventRequest | Event payload

begin
  # Publish outbound event
  result = api_instance.publish_outbound_event(publish_outbound_event_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling OutboundEventsApi->publish_outbound_event: #{e}"
end
```

#### Using the publish_outbound_event_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublishOutboundData>, Integer, Hash)> publish_outbound_event_with_http_info(publish_outbound_event_request)

```ruby
begin
  # Publish outbound event
  data, status_code, headers = api_instance.publish_outbound_event_with_http_info(publish_outbound_event_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublishOutboundData>
rescue Gethook::ApiError => e
  puts "Error when calling OutboundEventsApi->publish_outbound_event_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **publish_outbound_event_request** | [**PublishOutboundEventRequest**](PublishOutboundEventRequest.md) | Event payload |  |

### Return type

[**PublishOutboundData**](PublishOutboundData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## replay_outbound_event

> <ReplayEventData> replay_outbound_event(id)

Replay outbound event

### Examples

```ruby
require 'time'
require 'gethook'
# setup authorization
Gethook.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['Authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['Authorization'] = 'Bearer'
end

api_instance = Gethook::OutboundEventsApi.new
id = 'id_example' # String | Event UUID

begin
  # Replay outbound event
  result = api_instance.replay_outbound_event(id)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling OutboundEventsApi->replay_outbound_event: #{e}"
end
```

#### Using the replay_outbound_event_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReplayEventData>, Integer, Hash)> replay_outbound_event_with_http_info(id)

```ruby
begin
  # Replay outbound event
  data, status_code, headers = api_instance.replay_outbound_event_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReplayEventData>
rescue Gethook::ApiError => e
  puts "Error when calling OutboundEventsApi->replay_outbound_event_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Event UUID |  |

### Return type

[**ReplayEventData**](ReplayEventData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

