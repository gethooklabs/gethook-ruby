# Gethook::AuthApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**login**](AuthApi.md#login) | **POST** /v1/auth/login | Login with email and password |
| [**register**](AuthApi.md#register) | **POST** /v1/auth/register | Register with email and password |


## login

> <AccountBootstrapData> login(login_request)

Login with email and password

Authenticates with email/password and returns a fresh API key on success.

### Examples

```ruby
require 'time'
require 'gethook'

api_instance = Gethook::AuthApi.new
login_request = Gethook::LoginRequest.new({email: 'admin@example.com', password: 'supersecret'}) # LoginRequest | Login credentials

begin
  # Login with email and password
  result = api_instance.login(login_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling AuthApi->login: #{e}"
end
```

#### Using the login_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AccountBootstrapData>, Integer, Hash)> login_with_http_info(login_request)

```ruby
begin
  # Login with email and password
  data, status_code, headers = api_instance.login_with_http_info(login_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AccountBootstrapData>
rescue Gethook::ApiError => e
  puts "Error when calling AuthApi->login_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **login_request** | [**LoginRequest**](LoginRequest.md) | Login credentials |  |

### Return type

[**AccountBootstrapData**](AccountBootstrapData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## register

> <AccountBootstrapData> register(register_request)

Register with email and password

Creates a new account with email/password credentials and returns a bootstrap API key.

### Examples

```ruby
require 'time'
require 'gethook'

api_instance = Gethook::AuthApi.new
register_request = Gethook::RegisterRequest.new({email: 'admin@example.com', name: 'My Company', password: 'supersecret'}) # RegisterRequest | Registration details

begin
  # Register with email and password
  result = api_instance.register(register_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling AuthApi->register: #{e}"
end
```

#### Using the register_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AccountBootstrapData>, Integer, Hash)> register_with_http_info(register_request)

```ruby
begin
  # Register with email and password
  data, status_code, headers = api_instance.register_with_http_info(register_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AccountBootstrapData>
rescue Gethook::ApiError => e
  puts "Error when calling AuthApi->register_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **register_request** | [**RegisterRequest**](RegisterRequest.md) | Registration details |  |

### Return type

[**AccountBootstrapData**](AccountBootstrapData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

