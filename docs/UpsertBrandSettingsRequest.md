# Gethook::UpsertBrandSettingsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company_name** | **String** |  | [optional] |
| **docs_title** | **String** |  | [optional] |
| **logo_url** | **String** |  | [optional] |
| **primary_color** | **String** |  | [optional] |
| **support_email** | **String** |  | [optional] |

## Example

```ruby
require 'gethook'

instance = Gethook::UpsertBrandSettingsRequest.new(
  company_name: Acme Corp,
  docs_title: Acme Webhooks,
  logo_url: https://example.com/logo.png,
  primary_color: #6366f1,
  support_email: support@example.com
)
```

