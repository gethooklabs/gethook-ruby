# Gethook::EventsApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_event**](EventsApi.md#get_event) | **GET** /v1/events/{id} | Get inbound event |
| [**list_events**](EventsApi.md#list_events) | **GET** /v1/events | List inbound events |
| [**replay_event**](EventsApi.md#replay_event) | **POST** /v1/events/{id}/replay | Replay inbound event |


## get_event

> <EventDetailData> get_event(id)

Get inbound event

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

api_instance = Gethook::EventsApi.new
id = 'id_example' # String | Event UUID

begin
  # Get inbound event
  result = api_instance.get_event(id)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling EventsApi->get_event: #{e}"
end
```

#### Using the get_event_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EventDetailData>, Integer, Hash)> get_event_with_http_info(id)

```ruby
begin
  # Get inbound event
  data, status_code, headers = api_instance.get_event_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EventDetailData>
rescue Gethook::ApiError => e
  puts "Error when calling EventsApi->get_event_with_http_info: #{e}"
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


## list_events

> <EventListData> list_events(opts)

List inbound events

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

api_instance = Gethook::EventsApi.new
opts = {
  limit: 56, # Integer | Max results (default 25, max 200)
  offset: 56 # Integer | Pagination offset
}

begin
  # List inbound events
  result = api_instance.list_events(opts)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling EventsApi->list_events: #{e}"
end
```

#### Using the list_events_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EventListData>, Integer, Hash)> list_events_with_http_info(opts)

```ruby
begin
  # List inbound events
  data, status_code, headers = api_instance.list_events_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EventListData>
rescue Gethook::ApiError => e
  puts "Error when calling EventsApi->list_events_with_http_info: #{e}"
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


## replay_event

> <ReplayEventData> replay_event(id)

Replay inbound event

Creates a new queued copy of the event for re-delivery.

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

api_instance = Gethook::EventsApi.new
id = 'id_example' # String | Event UUID

begin
  # Replay inbound event
  result = api_instance.replay_event(id)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling EventsApi->replay_event: #{e}"
end
```

#### Using the replay_event_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReplayEventData>, Integer, Hash)> replay_event_with_http_info(id)

```ruby
begin
  # Replay inbound event
  data, status_code, headers = api_instance.replay_event_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReplayEventData>
rescue Gethook::ApiError => e
  puts "Error when calling EventsApi->replay_event_with_http_info: #{e}"
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

