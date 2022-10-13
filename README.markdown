# Rubocop Config

This repo includes Rubocop (https://rubocop.org/) config shared across all Burt's Ruby projects.

## Usage

Install the Rubocop gems (which one depends on the type of project).

```ruby
group :development do
  gem 'rubocop'
  gem 'rubocop-rails'
  gem 'rubocop-rspec'
end
```

Add the Rubocop config in `.rubocop.yml`:

```yaml
inherit_from:
  - https://raw.githubusercontent.com/burtcorp/rubocop-config/master/rubocop.yml
  - https://raw.githubusercontent.com/burtcorp/rubocop-config/master/rubocop-rspec.yml

AllCops:
  TargetRubyVersion: 3.1

Style/TrailingBodyOnModule:
  Enabled: false

# ...
```
