# Gethook::RoutesApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_route**](RoutesApi.md#create_route) | **POST** /v1/routes | Create route |
| [**list_routes**](RoutesApi.md#list_routes) | **GET** /v1/routes | List routes |


## create_route

> <Route> create_route(create_route_request)

Create route

Creates a routing rule that forwards matching events from a source to a destination.

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

api_instance = Gethook::RoutesApi.new
create_route_request = Gethook::CreateRouteRequest.new({destination_id: 'uuid'}) # CreateRouteRequest | Route config

begin
  # Create route
  result = api_instance.create_route(create_route_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling RoutesApi->create_route: #{e}"
end
```

#### Using the create_route_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Route>, Integer, Hash)> create_route_with_http_info(create_route_request)

```ruby
begin
  # Create route
  data, status_code, headers = api_instance.create_route_with_http_info(create_route_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Route>
rescue Gethook::ApiError => e
  puts "Error when calling RoutesApi->create_route_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_route_request** | [**CreateRouteRequest**](CreateRouteRequest.md) | Route config |  |

### Return type

[**Route**](Route.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_routes

> <Array<Route>> list_routes

List routes

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

api_instance = Gethook::RoutesApi.new

begin
  # List routes
  result = api_instance.list_routes
  p result
rescue Gethook::ApiError => e
  puts "Error when calling RoutesApi->list_routes: #{e}"
end
```

#### Using the list_routes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Route>>, Integer, Hash)> list_routes_with_http_info

```ruby
begin
  # List routes
  data, status_code, headers = api_instance.list_routes_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Route>>
rescue Gethook::ApiError => e
  puts "Error when calling RoutesApi->list_routes_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;Route&gt;**](Route.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

