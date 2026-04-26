# Gethook::CustomDomainsApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_custom_domain**](CustomDomainsApi.md#create_custom_domain) | **POST** /v1/custom-domains | Create custom domain |
| [**list_custom_domains**](CustomDomainsApi.md#list_custom_domains) | **GET** /v1/custom-domains | List custom domains |


## create_custom_domain

> <CustomDomain> create_custom_domain(create_custom_domain_request)

Create custom domain

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

api_instance = Gethook::CustomDomainsApi.new
create_custom_domain_request = Gethook::CreateCustomDomainRequest.new({domain: 'webhooks.example.com'}) # CreateCustomDomainRequest | Domain details

begin
  # Create custom domain
  result = api_instance.create_custom_domain(create_custom_domain_request)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling CustomDomainsApi->create_custom_domain: #{e}"
end
```

#### Using the create_custom_domain_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomDomain>, Integer, Hash)> create_custom_domain_with_http_info(create_custom_domain_request)

```ruby
begin
  # Create custom domain
  data, status_code, headers = api_instance.create_custom_domain_with_http_info(create_custom_domain_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomDomain>
rescue Gethook::ApiError => e
  puts "Error when calling CustomDomainsApi->create_custom_domain_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_custom_domain_request** | [**CreateCustomDomainRequest**](CreateCustomDomainRequest.md) | Domain details |  |

### Return type

[**CustomDomain**](CustomDomain.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_custom_domains

> <Array<CustomDomain>> list_custom_domains

List custom domains

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

api_instance = Gethook::CustomDomainsApi.new

begin
  # List custom domains
  result = api_instance.list_custom_domains
  p result
rescue Gethook::ApiError => e
  puts "Error when calling CustomDomainsApi->list_custom_domains: #{e}"
end
```

#### Using the list_custom_domains_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<CustomDomain>>, Integer, Hash)> list_custom_domains_with_http_info

```ruby
begin
  # List custom domains
  data, status_code, headers = api_instance.list_custom_domains_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<CustomDomain>>
rescue Gethook::ApiError => e
  puts "Error when calling CustomDomainsApi->list_custom_domains_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;CustomDomain&gt;**](CustomDomain.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

