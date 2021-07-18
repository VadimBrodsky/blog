---
layout: post
title: Rails Credentials Command
date: 2021-04-26 06:37 -0400
tags: rails
---
To edit the credentials file, run the `credentials:edit` command[^1]:

> By default, the credentials file contains the application's `secret_key_base`. It can also be used to store other secrets such as access keys for external APIs.

> Additionally, this command will create `config/master.key` if no master key is defined.

```bash
bin/rails credentials:edit
bin/rails credentials:edit --environment=production
```

[^1]: [Custom Credentials - RailsGuides](https://edgeguides.rubyonrails.org/security.html#custom-credentials)
