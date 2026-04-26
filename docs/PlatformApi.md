# Gethook::PlatformApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_platform_stats**](PlatformApi.md#get_platform_stats) | **GET** /v1/platform-stats | Public platform statistics |


## get_platform_stats

> <PlatformStats> get_platform_stats

Public platform statistics

### Examples

```ruby
require 'time'
require 'gethook'

api_instance = Gethook::PlatformApi.new

begin
  # Public platform statistics
  result = api_instance.get_platform_stats
  p result
rescue Gethook::ApiError => e
  puts "Error when calling PlatformApi->get_platform_stats: #{e}"
end
```

#### Using the get_platform_stats_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PlatformStats>, Integer, Hash)> get_platform_stats_with_http_info

```ruby
begin
  # Public platform statistics
  data, status_code, headers = api_instance.get_platform_stats_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PlatformStats>
rescue Gethook::ApiError => e
  puts "Error when calling PlatformApi->get_platform_stats_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**PlatformStats**](PlatformStats.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

