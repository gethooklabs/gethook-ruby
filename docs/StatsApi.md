# Gethook::StatsApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_stats**](StatsApi.md#get_stats) | **GET** /v1/stats | Get dashboard stats |


## get_stats

> <StatsData> get_stats

Get dashboard stats

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

api_instance = Gethook::StatsApi.new

begin
  # Get dashboard stats
  result = api_instance.get_stats
  p result
rescue Gethook::ApiError => e
  puts "Error when calling StatsApi->get_stats: #{e}"
end
```

#### Using the get_stats_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StatsData>, Integer, Hash)> get_stats_with_http_info

```ruby
begin
  # Get dashboard stats
  data, status_code, headers = api_instance.get_stats_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StatsData>
rescue Gethook::ApiError => e
  puts "Error when calling StatsApi->get_stats_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**StatsData**](StatsData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

