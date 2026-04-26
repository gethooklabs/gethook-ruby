# Gethook::ApiKeysApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_api_key**](ApiKeysApi.md#create_api_key) | **POST** /v1/api-keys | Create API key |
| [**delete_api_key**](ApiKeysApi.md#delete_api_key) | **DELETE** /v1/api-keys/{id} | Revoke API key |
| [**list_api_keys**](ApiKeysApi.md#list_api_keys) | **GET** /v1/api-keys | List API keys |


## create_api_key

> <APIKeyWithSecret> create_api_key(create_api_key_request)

Create API key

Creates a new API key for the authenticated account. The full key is only returned once.

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

api_instance = Gethook::ApiKeysApi.new
create_api_key_request = Gethook::CreateAPIKeyRequest.new({name: 'production'}) # CreateAPIKeyRequest | Key name

begin
  # Create API key
  result = api_instance.create_api_key(create_api_key_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling ApiKeysApi->create_api_key: #{e}"
end
```

#### Using the create_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<APIKeyWithSecret>, Integer, Hash)> create_api_key_with_http_info(create_api_key_request)

```ruby
begin
  # Create API key
  data, status_code, headers = api_instance.create_api_key_with_http_info(create_api_key_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <APIKeyWithSecret>
rescue Gethook::ApiError => e
  puts "Error when calling ApiKeysApi->create_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_api_key_request** | [**CreateAPIKeyRequest**](CreateAPIKeyRequest.md) | Key name |  |

### Return type

[**APIKeyWithSecret**](APIKeyWithSecret.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_api_key

> delete_api_key(id)

Revoke API key

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

api_instance = Gethook::ApiKeysApi.new
id = 'id_example' # String | API key UUID

begin
  # Revoke API key
  api_instance.delete_api_key(id)
rescue Gethook::ApiError => e
  puts "Error when calling ApiKeysApi->delete_api_key: #{e}"
end
```

#### Using the delete_api_key_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_api_key_with_http_info(id)

```ruby
begin
  # Revoke API key
  data, status_code, headers = api_instance.delete_api_key_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Gethook::ApiError => e
  puts "Error when calling ApiKeysApi->delete_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | API key UUID |  |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_api_keys

> <Array<APIKey>> list_api_keys

List API keys

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

api_instance = Gethook::ApiKeysApi.new

begin
  # List API keys
  result = api_instance.list_api_keys
  p result
rescue Gethook::ApiError => e
  puts "Error when calling ApiKeysApi->list_api_keys: #{e}"
end
```

#### Using the list_api_keys_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<APIKey>>, Integer, Hash)> list_api_keys_with_http_info

```ruby
begin
  # List API keys
  data, status_code, headers = api_instance.list_api_keys_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<APIKey>>
rescue Gethook::ApiError => e
  puts "Error when calling ApiKeysApi->list_api_keys_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;APIKey&gt;**](APIKey.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

