# Gethook::SourcesApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_source**](SourcesApi.md#create_source) | **POST** /v1/sources | Create source |
| [**delete_source**](SourcesApi.md#delete_source) | **DELETE** /v1/sources/{id} | Delete source |
| [**get_source**](SourcesApi.md#get_source) | **GET** /v1/sources/{id} | Get source |
| [**list_providers**](SourcesApi.md#list_providers) | **GET** /v1/provider-presets | List provider presets |
| [**list_sources**](SourcesApi.md#list_sources) | **GET** /v1/sources | List sources |


## create_source

> <Source> create_source(create_source_request)

Create source

Creates a new webhook source endpoint. Returns an ingest_url to share with the event sender.

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

api_instance = Gethook::SourcesApi.new
create_source_request = Gethook::CreateSourceRequest.new({name: 'Stripe webhooks'}) # CreateSourceRequest | Source config

begin
  # Create source
  result = api_instance.create_source(create_source_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling SourcesApi->create_source: #{e}"
end
```

#### Using the create_source_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Source>, Integer, Hash)> create_source_with_http_info(create_source_request)

```ruby
begin
  # Create source
  data, status_code, headers = api_instance.create_source_with_http_info(create_source_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Source>
rescue Gethook::ApiError => e
  puts "Error when calling SourcesApi->create_source_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_source_request** | [**CreateSourceRequest**](CreateSourceRequest.md) | Source config |  |

### Return type

[**Source**](Source.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_source

> delete_source(id)

Delete source

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

api_instance = Gethook::SourcesApi.new
id = 'id_example' # String | Source UUID

begin
  # Delete source
  api_instance.delete_source(id)
rescue Gethook::ApiError => e
  puts "Error when calling SourcesApi->delete_source: #{e}"
end
```

#### Using the delete_source_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_source_with_http_info(id)

```ruby
begin
  # Delete source
  data, status_code, headers = api_instance.delete_source_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Gethook::ApiError => e
  puts "Error when calling SourcesApi->delete_source_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Source UUID |  |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_source

> <Source> get_source(id)

Get source

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

api_instance = Gethook::SourcesApi.new
id = 'id_example' # String | Source UUID

begin
  # Get source
  result = api_instance.get_source(id)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling SourcesApi->get_source: #{e}"
end
```

#### Using the get_source_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Source>, Integer, Hash)> get_source_with_http_info(id)

```ruby
begin
  # Get source
  data, status_code, headers = api_instance.get_source_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Source>
rescue Gethook::ApiError => e
  puts "Error when calling SourcesApi->get_source_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Source UUID |  |

### Return type

[**Source**](Source.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_providers

> <Array<ProviderPreset>> list_providers

List provider presets

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

api_instance = Gethook::SourcesApi.new

begin
  # List provider presets
  result = api_instance.list_providers
  p result
rescue Gethook::ApiError => e
  puts "Error when calling SourcesApi->list_providers: #{e}"
end
```

#### Using the list_providers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ProviderPreset>>, Integer, Hash)> list_providers_with_http_info

```ruby
begin
  # List provider presets
  data, status_code, headers = api_instance.list_providers_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ProviderPreset>>
rescue Gethook::ApiError => e
  puts "Error when calling SourcesApi->list_providers_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;ProviderPreset&gt;**](ProviderPreset.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_sources

> <Array<Source>> list_sources

List sources

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

api_instance = Gethook::SourcesApi.new

begin
  # List sources
  result = api_instance.list_sources
  p result
rescue Gethook::ApiError => e
  puts "Error when calling SourcesApi->list_sources: #{e}"
end
```

#### Using the list_sources_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Source>>, Integer, Hash)> list_sources_with_http_info

```ruby
begin
  # List sources
  data, status_code, headers = api_instance.list_sources_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Source>>
rescue Gethook::ApiError => e
  puts "Error when calling SourcesApi->list_sources_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;Source&gt;**](Source.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

