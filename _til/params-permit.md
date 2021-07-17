---
layout: post
title: Params permit!
date: 2021-04-26 13:10 -0400
tags: rails
---

A method[^1] that sets the `permitted` attribute to `true`.
- Used to pass mass assignment.
- Needs to be used with caution.

```ruby
class Person < ActiveRecord::Base
end
```

```ruby
params = ActionController::Parameters.new(name: "Francesco")
params.permitted?  # => false
Person.new(params) # => ActiveModel::ForbiddenAttributesError
params.permit!
params.permitted?  # => true
Person.new(params) # => #<Person id: nil, name: "Francesco">
```

[^1]: [ActionController::Parameters#permit!](https://api.rubyonrails.org/classes/ActionController/Parameters.html#method-i-permit-21)
