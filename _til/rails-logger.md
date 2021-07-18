---
layout: post
title: Rails Logger
date: 2021-04-26 06:09 -0400
tags: rails
---
Rails makes use[^1] of the `ActiveSupport::Logger` class[^2] to write log information.

```ruby
Rails.logger.debug "Person attributes hash: #{@person.attributes.inspect}"
Rails.logger.info "Processing the request..."
Rails.logger.fatal "Terminating application, raised unrecoverable error!!!"
```

[^1]: [What is the Logger? - Rails Guides](https://guides.rubyonrails.org/debugging_rails_applications.html#what-is-the-logger-questionmark)
[^2]: [ActiveSupport::Logger](https://api.rubyonrails.org/classes/ActiveSupport/Logger.html)
