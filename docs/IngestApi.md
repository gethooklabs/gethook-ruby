# Gethook::IngestApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**ingest**](IngestApi.md#ingest) | **POST** /ingest/{token} | Ingest webhook event |


## ingest

> <IngestAcceptedData> ingest(token)

Ingest webhook event

Accepts an inbound webhook. The path token authenticates the source — no Bearer header required.

### Examples

```ruby
require 'time'
require 'gethook'

api_instance = Gethook::IngestApi.new
token = 'token_example' # String | Source path token (src_...)

begin
  # Ingest webhook event
  result = api_instance.ingest(token)
  p result
rescue Gethook::ApiError => e
  puts "Error when calling IngestApi->ingest: #{e}"
end
```

#### Using the ingest_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<IngestAcceptedData>, Integer, Hash)> ingest_with_http_info(token)

```ruby
begin
  # Ingest webhook event
  data, status_code, headers = api_instance.ingest_with_http_info(token)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <IngestAcceptedData>
rescue Gethook::ApiError => e
  puts "Error when calling IngestApi->ingest_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **token** | **String** | Source path token (src_...) |  |

### Return type

[**IngestAcceptedData**](IngestAcceptedData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

