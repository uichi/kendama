# kendama

Kendama - the Ruby gem for the 国税庁API

No description provided (generated by Openapi Generator https://github.com/openapitools/openapi-generator)

This SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- Package version: 0.2.1
- Build package: org.openapitools.codegen.languages.RubyClientCodegen

## Installation

### Build a gem

To build the Ruby code into a gem:

```shell
gem build kendama.gemspec
```

Then either install the gem locally:

```shell
gem install ./kendama-0.2.1.gem
```

(for development, run `gem install --dev ./kendama-0.2.1.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the Gemfile:

    gem 'kendama', '~> 0.2.1'

### Install from Git

If the Ruby gem is hosted at a git repository: https://github.com/GIT_USER_ID/GIT_REPO_ID, then add the following in the Gemfile:

    gem 'kendama', :git => 'https://github.com/GIT_USER_ID/GIT_REPO_ID.git'

### Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

```shell
ruby -Ilib script.rb
```

## Getting Started

Please follow the [installation](#installation) procedure and then run the following code:

```ruby
# Load the gem
require 'kendama'

api_instance = Kendama::V1Api.new
id = 'id_example' # String | 
from = Date.parse('Tue Oct 01 09:00:00 JST 2024') # Date | 
to = Date.parse('Tue Oct 01 09:00:00 JST 2024') # Date | 
type = '21' # String | 
opts = {
  division: '1', # String | 
  divide: 'divide_example' # String | 
}

begin
  #取得期間を指定して情報を取得
  result = api_instance.get_announcement_by_diff(id, from, to, type, opts)
  p result
rescue Kendama::ApiError => e
  puts "Exception when calling V1Api->get_announcement_by_diff: #{e}"
end

```

## Documentation for API Endpoints

All URIs are relative to *https://kensyo.invoice-kohyo.nta.go.jp*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*Kendama::V1Api* | [**get_announcement_by_diff**](docs/V1Api.md#get_announcement_by_diff) | **GET** /1/diff | 取得期間を指定して情報を取得
*Kendama::V1Api* | [**get_announcement_by_number**](docs/V1Api.md#get_announcement_by_number) | **GET** /1/num | 登録番号を指定して情報を取得
*Kendama::V1Api* | [**get_announcement_by_valid**](docs/V1Api.md#get_announcement_by_valid) | **GET** /1/valid | 登録番号と日付を指定して情報を取得


## Documentation for Models

 - [Kendama::Announcement](docs/Announcement.md)
 - [Kendama::ResponseBody](docs/ResponseBody.md)


## Documentation for Authorization

Endpoints do not require authorization.

