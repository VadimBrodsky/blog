---
layout: post
title: 'Ruby Load Path $:'
tags: ruby
date: 2021-04-24 06:04 -0400
---
The paths for loading code in Ruby are stored in the global load path `$:` or `$LOAD_PATH` variables[^1]

```bash
vadim@devbuntu ~/c/s/ruby> ruby -e 'puts $:'
/home/vadim/.asdf/plugins/ruby/rubygems-plugin
/home/vadim/.asdf/installs/ruby/3.0.0/lib/ruby/site_ruby/3.0.0
/home/vadim/.asdf/installs/ruby/3.0.0/lib/ruby/site_ruby/3.0.0/x86_64-linux
/home/vadim/.asdf/installs/ruby/3.0.0/lib/ruby/site_ruby
/home/vadim/.asdf/installs/ruby/3.0.0/lib/ruby/vendor_ruby/3.0.0
/home/vadim/.asdf/installs/ruby/3.0.0/lib/ruby/vendor_ruby/3.0.0/x86_64-linux
/home/vadim/.asdf/installs/ruby/3.0.0/lib/ruby/vendor_ruby
/home/vadim/.asdf/installs/ruby/3.0.0/lib/ruby/3.0.0
/home/vadim/.asdf/installs/ruby/3.0.0/lib/ruby/3.0.0/x86_64-linux
```

can add[^2] to the load paths same was as in the shell

```ruby
$: << File.expand_path
```

[^1]: [Pre-defined global variabled - RubyDoc 3.0.0](https://docs.ruby-lang.org/en/3.0.0/doc/globals_rdoc.html)
[^2]: [what is “$:” in ruby? - StackOverflow.com](https://stackoverflow.com/questions/7846426/what-is-in-ruby)
