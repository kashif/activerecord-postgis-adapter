# Contributing

Fork the repo:

`git clone git@github.com:rgeo/activerecord-postgis-adapter.git`

Set up your test database:

```sh
createdb postgis_adapter_test
createuser -s postgres
psql postgis_adapter_test
=# CREATE EXTENSION postgis;
```

Make sure the tests pass:

`rake`

Run tests against ActiveRecord 4.0, 4.1 and 4.2 test gemfiles:

run `appraisal rake` or run the tests manually:

```
BUNDLE_GEMFILE=./gemfiles/ar40.gemfile bundle
BUNDLE_GEMFILE=./gemfiles/ar40.gemfile rake

BUNDLE_GEMFILE=./gemfiles/ar41.gemfile bundle
BUNDLE_GEMFILE=./gemfiles/ar41.gemfile rake

BUNDLE_GEMFILE=./gemfiles/ar42.gemfile bundle
BUNDLE_GEMFILE=./gemfiles/ar42.gemfile rake
```

Make your changes and submit a pull request.
