[![Build Status](https://secure.travis-ci.org/dtaniwaki/fluent-plugin-fork.png?branch=master)](http://travis-ci.org/dtaniwaki/fluent-plugin-fork)

# fluent-plugin-fork

Fork output by separating values for fluentd

# Installation

## td-agent(Linux)

```
/usr/lib64/fluent/ruby/bin/fluent-gem install fluent-plugin-fork
```

## td-agent(Mac)

```
sudo /usr/local/Cellar/td-agent/1.1.XX/bin/fluent-gem install fluent-plugin-fork
```

## fluentd only

```
gem install fluent-plugin-fork
```

# Configuration

```
output_tag   tag_to_output
output_key   key_to_output
separator    ,
fork_key     key_to_fork
max_size     15
max_fallback log
no_unique    true
```

## output_tag

Tag to output forked values

## output_key

Key name to output forked values

## fork_key

Key name to fork

## separator (Optional)

Separator to separate the values

Default: ,

## max_size (Optional)

Max size of forked values.

Default: nil

## max_fallback (Optional)

Strategy when the size of values exceeds max_size. Only effective when you set max_size.

`log` to log the record
`drop` to drop exceeded values

Default: log

## no_unique (Optional)

Flag to emit redundant values.

Default: false

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new [Pull Request](../../pull/new/master)

## Copyright

Copyright (c) 2014 Daisuke Taniwaki. See [LICENSE](LICENSE) for details.