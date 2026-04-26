# Gethook::AccountsApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_account**](AccountsApi.md#create_account) | **POST** /v1/accounts | Create account |


## create_account

> <AccountBootstrapData> create_account(create_account_request)

Create account

Creates a new account and returns a bootstrap API key. No authentication required.

### Examples

```ruby
require 'time'
require 'gethook'

api_instance = Gethook::AccountsApi.new
create_account_request = Gethook::CreateAccountRequest.new({name: 'My Company'}) # CreateAccountRequest | Account name

begin
  # Create account
  result = api_instance.create_account(create_account_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling AccountsApi->create_account: #{e}"
end
```

#### Using the create_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AccountBootstrapData>, Integer, Hash)> create_account_with_http_info(create_account_request)

```ruby
begin
  # Create account
  data, status_code, headers = api_instance.create_account_with_http_info(create_account_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AccountBootstrapData>
rescue Gethook::ApiError => e
  puts "Error when calling AccountsApi->create_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_account_request** | [**CreateAccountRequest**](CreateAccountRequest.md) | Account name |  |

### Return type

[**AccountBootstrapData**](AccountBootstrapData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

