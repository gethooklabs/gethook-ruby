# Gethook::HealthApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**healthz**](HealthApi.md#healthz) | **GET** /healthz | Liveness check |
| [**readyz**](HealthApi.md#readyz) | **GET** /readyz | Readiness check |


## healthz

> Hash&lt;String, String&gt; healthz

Liveness check

### Examples

```ruby
require 'time'
require 'gethook'

api_instance = Gethook::HealthApi.new

begin
  # Liveness check
  result = api_instance.healthz
  p result
rescue Gethook::ApiError => e
  puts "Error when calling HealthApi->healthz: #{e}"
end
```

#### Using the healthz_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, String&gt;, Integer, Hash)> healthz_with_http_info

```ruby
begin
  # Liveness check
  data, status_code, headers = api_instance.healthz_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, String&gt;
rescue Gethook::ApiError => e
  puts "Error when calling HealthApi->healthz_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Hash&lt;String, String&gt;**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## readyz

> Hash&lt;String, String&gt; readyz

Readiness check

### Examples

```ruby
require 'time'
require 'gethook'

api_instance = Gethook::HealthApi.new

begin
  # Readiness check
  result = api_instance.readyz
  p result
rescue Gethook::ApiError => e
  puts "Error when calling HealthApi->readyz: #{e}"
end
```

#### Using the readyz_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, String&gt;, Integer, Hash)> readyz_with_http_info

```ruby
begin
  # Readiness check
  data, status_code, headers = api_instance.readyz_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, String&gt;
rescue Gethook::ApiError => e
  puts "Error when calling HealthApi->readyz_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Hash&lt;String, String&gt;**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

