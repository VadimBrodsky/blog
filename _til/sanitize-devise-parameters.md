---
layout: post
title: Sanitize Devise Parameters
date: 2021-04-27 06:41 -0400
tags: rails devise
---

To use custom fields on the Devise User model[^1] these fields need to be allowed because of strong parameters.

```ruby
class ApplicationController < ActionController::Base
  before_action :configure_permitted_parameters, if: :devise_controller?

  protected

  def configure_permitted_parameters
    # Permit the `subscribe_newsletter` parameter along with the other
    # sign up parameters.
    devise_parameter_sanitizer.permit(:sign_up, keys: [:subscribe_newsletter])
  end
end
```

[^1]: [Class: Devise::ParameterSanitizer](https://www.rubydoc.info/github/plataformatec/devise/Devise/ParameterSanitizer)
