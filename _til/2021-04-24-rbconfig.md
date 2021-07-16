---
layout: post
title: RbConfig
tags: ruby
date: 2021-04-24T14:10:00.000Z
---
Presents the configuration[^1] for the current Ruby installation.

```bash
irb --simple-prompt -r -rbconfig
```

Requires the `rbconfig` module in an `irb` session

```ruby
RbConfig::CONFIG['bindir']
=> "/home/vadim/.asdf/installs/ruby/3.0.0/bin"
```

Other useful keys in the `CONFIG` hash:

- `rubylibdir` - Ruby standard library
- `bindir` - Ruby command-line tools
- `archdir` - Architecture specific extensions and libraries (compiled, binary files)
- `sitedir` - Your own or third-party extensions and libraries (written in Ruby)
- `vendordir` - Third party extensions and libraries (written in Ruby)
- `sitelibdir` - Your own Ruby language extensions (written in Ruby)
- `sitearchdir` - Your own Ruby language extensions (written in C)

[^1]: [Module:RbConfig - RubyDoc](https://www.rubydoc.info/github/rubyworks/facets/RbConfig)
