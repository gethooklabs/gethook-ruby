# Gethook::DestinationPreset

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auth_header** | **String** | for api_key type | [optional] |
| **auth_label** | **String** | e.g. \&quot;Bot Token\&quot;, \&quot;API Key\&quot; | [optional] |
| **auth_type** | **String** | \&quot;none\&quot;, \&quot;bearer\&quot;, \&quot;api_key\&quot; | [optional] |
| **category** | **String** |  | [optional] |
| **color** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **docs_url** | **String** |  | [optional] |
| **extra_headers** | **Hash&lt;String, String&gt;** |  | [optional] |
| **id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **url_hint** | **String** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::DestinationPreset.new(
  auth_header: null,
  auth_label: null,
  auth_type: null,
  category: null,
  color: null,
  description: null,
  docs_url: null,
  extra_headers: null,
  id: null,
  name: null,
  url_hint: null
)
```

