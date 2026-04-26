# Gethook::BrandApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_brand_settings**](BrandApi.md#get_brand_settings) | **GET** /v1/brand-settings | Get brand settings |
| [**upsert_brand_settings**](BrandApi.md#upsert_brand_settings) | **POST** /v1/brand-settings | Upsert brand settings |


## get_brand_settings

> <BrandSettings> get_brand_settings

Get brand settings

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

api_instance = Gethook::BrandApi.new

begin
  # Get brand settings
  result = api_instance.get_brand_settings
  p result
rescue Gethook::ApiError => e
  puts "Error when calling BrandApi->get_brand_settings: #{e}"
end
```

#### Using the get_brand_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandSettings>, Integer, Hash)> get_brand_settings_with_http_info

```ruby
begin
  # Get brand settings
  data, status_code, headers = api_instance.get_brand_settings_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandSettings>
rescue Gethook::ApiError => e
  puts "Error when calling BrandApi->get_brand_settings_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**BrandSettings**](BrandSettings.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## upsert_brand_settings

> <BrandSettings> upsert_brand_settings(upsert_brand_settings_request)

Upsert brand settings

Creates or replaces white-label brand settings for the account.

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

api_instance = Gethook::BrandApi.new
upsert_brand_settings_request = Gethook::UpsertBrandSettingsRequest.new # UpsertBrandSettingsRequest | Brand settings

begin
  # Upsert brand settings
  result = api_instance.upsert_brand_settings(upsert_brand_settings_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling BrandApi->upsert_brand_settings: #{e}"
end
```

#### Using the upsert_brand_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandSettings>, Integer, Hash)> upsert_brand_settings_with_http_info(upsert_brand_settings_request)

```ruby
begin
  # Upsert brand settings
  data, status_code, headers = api_instance.upsert_brand_settings_with_http_info(upsert_brand_settings_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandSettings>
rescue Gethook::ApiError => e
  puts "Error when calling BrandApi->upsert_brand_settings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **upsert_brand_settings_request** | [**UpsertBrandSettingsRequest**](UpsertBrandSettingsRequest.md) | Brand settings |  |

### Return type

[**BrandSettings**](BrandSettings.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

