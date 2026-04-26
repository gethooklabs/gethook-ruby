# gethook-ruby — Ruby SDK

Ruby client for the [GetHook](https://gethook.to) Webhook Reliability Gateway API.

## Installation

```bash
gem install gethook
```

Or in your Gemfile:
```ruby
gem 'gethook', '~> 0.1'
```

## Usage

```ruby
require 'gethook'

Gethook.configure do |config|
  config.host = 'api.gethook.to'
  config.api_key['ApiKeyAuth'] = 'hk_your_api_key'
end

api = Gethook::SourcesApi.new
sources = api.list_sources
puts sources
```

## Documentation

Full API reference: https://docs.gethook.to/reference

## Development

This SDK is auto-generated from the OpenAPI spec via `make sync` in the main [gethook](https://github.com/gethook/gethook) repo.
