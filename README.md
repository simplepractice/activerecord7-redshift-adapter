activerecord7-redshift-adapter
==============================

Amazon Redshift adapter for ActiveRecord 7 (Rails 7).
This is a fork from https://rubygems.org/gems/activerecord7-redshift-adapter hosted on a private Gitlab instance.
It's itself forked the project from https://github.com/kwent/activerecord6-redshift-adapter

Thanks to the auhors.

Usage
-------------------

For Rails 7, write following in Gemfile:

```ruby
git_source(:fork) { |name| "https://github.com/simplepractice/#{name}.git" }

gem 'activerecord7-redshift-adapter', fork: 'activerecord7-redshift-adapter'
```

In database.yml

```YAML
development:
  adapter: redshift
  host: host
  port: port
  database: db
  username: user
  password: password
  encoding: utf8
```

OR your can use in URL
```ruby
class SomeModel < ApplicationRecord
  establish_connection('redshift://username:password@host/database')
end
```

License
---------

MIT license (same as ActiveRecord)
