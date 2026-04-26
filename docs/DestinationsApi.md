# Gethook::DestinationsApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_destination**](DestinationsApi.md#create_destination) | **POST** /v1/destinations | Create destination |
| [**get_destination**](DestinationsApi.md#get_destination) | **GET** /v1/destinations/{id} | Get destination |
| [**list_destination_presets**](DestinationsApi.md#list_destination_presets) | **GET** /v1/destination-presets | List destination presets |
| [**list_destinations**](DestinationsApi.md#list_destinations) | **GET** /v1/destinations | List destinations |
| [**rotate_destination_secret**](DestinationsApi.md#rotate_destination_secret) | **POST** /v1/destinations/{id}/rotate-secret | Rotate destination signing secret |
| [**update_destination**](DestinationsApi.md#update_destination) | **PATCH** /v1/destinations/{id} | Update destination |


## create_destination

> <Destination> create_destination(create_destination_request)

Create destination

Creates a new webhook delivery destination. The signing_secret is encrypted at rest and never returned.

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

api_instance = Gethook::DestinationsApi.new
create_destination_request = Gethook::CreateDestinationRequest.new({name: 'My endpoint', url: 'https://example.com/webhooks'}) # CreateDestinationRequest | Destination config

begin
  # Create destination
  result = api_instance.create_destination(create_destination_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->create_destination: #{e}"
end
```

#### Using the create_destination_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Destination>, Integer, Hash)> create_destination_with_http_info(create_destination_request)

```ruby
begin
  # Create destination
  data, status_code, headers = api_instance.create_destination_with_http_info(create_destination_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Destination>
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->create_destination_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_destination_request** | [**CreateDestinationRequest**](CreateDestinationRequest.md) | Destination config |  |

### Return type

[**Destination**](Destination.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_destination

> <Destination> get_destination(id)

Get destination

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

api_instance = Gethook::DestinationsApi.new
id = 'id_example' # String | Destination UUID

begin
  # Get destination
  result = api_instance.get_destination(id)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->get_destination: #{e}"
end
```

#### Using the get_destination_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Destination>, Integer, Hash)> get_destination_with_http_info(id)

```ruby
begin
  # Get destination
  data, status_code, headers = api_instance.get_destination_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Destination>
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->get_destination_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Destination UUID |  |

### Return type

[**Destination**](Destination.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_destination_presets

> <Array<DestinationPreset>> list_destination_presets

List destination presets

### Examples

```ruby
require 'time'
require 'gethook'

api_instance = Gethook::DestinationsApi.new

begin
  # List destination presets
  result = api_instance.list_destination_presets
  p result
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->list_destination_presets: #{e}"
end
```

#### Using the list_destination_presets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<DestinationPreset>>, Integer, Hash)> list_destination_presets_with_http_info

```ruby
begin
  # List destination presets
  data, status_code, headers = api_instance.list_destination_presets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<DestinationPreset>>
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->list_destination_presets_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;DestinationPreset&gt;**](DestinationPreset.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_destinations

> <Array<Destination>> list_destinations

List destinations

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

api_instance = Gethook::DestinationsApi.new

begin
  # List destinations
  result = api_instance.list_destinations
  p result
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->list_destinations: #{e}"
end
```

#### Using the list_destinations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Destination>>, Integer, Hash)> list_destinations_with_http_info

```ruby
begin
  # List destinations
  data, status_code, headers = api_instance.list_destinations_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Destination>>
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->list_destinations_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;Destination&gt;**](Destination.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## rotate_destination_secret

> Object rotate_destination_secret(id, body)

Rotate destination signing secret

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

api_instance = Gethook::DestinationsApi.new
id = 'id_example' # String | Destination UUID
body = { ... } # Object | New signing secret

begin
  # Rotate destination signing secret
  result = api_instance.rotate_destination_secret(id, body)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->rotate_destination_secret: #{e}"
end
```

#### Using the rotate_destination_secret_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> rotate_destination_secret_with_http_info(id, body)

```ruby
begin
  # Rotate destination signing secret
  data, status_code, headers = api_instance.rotate_destination_secret_with_http_info(id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->rotate_destination_secret_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Destination UUID |  |
| **body** | **Object** | New signing secret |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_destination

> <Destination> update_destination(id, update_destination_request)

Update destination

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

api_instance = Gethook::DestinationsApi.new
id = 'id_example' # String | Destination UUID
update_destination_request = Gethook::UpdateDestinationRequest.new # UpdateDestinationRequest | Fields to update

begin
  # Update destination
  result = api_instance.update_destination(id, update_destination_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->update_destination: #{e}"
end
```

#### Using the update_destination_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Destination>, Integer, Hash)> update_destination_with_http_info(id, update_destination_request)

```ruby
begin
  # Update destination
  data, status_code, headers = api_instance.update_destination_with_http_info(id, update_destination_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Destination>
rescue Gethook::ApiError => e
  puts "Error when calling DestinationsApi->update_destination_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Destination UUID |  |
| **update_destination_request** | [**UpdateDestinationRequest**](UpdateDestinationRequest.md) | Fields to update |  |

### Return type

[**Destination**](Destination.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

