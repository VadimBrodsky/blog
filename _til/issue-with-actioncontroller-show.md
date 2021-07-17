---
layout: post
title: Issue with ActionController#show
date: 2021-04-26 06:02 -0400
tags: rails
---
Could not get the `show` action to pass the `@user` instance variable into the view. Thought the issue was with in inheriting from `Clearance`[^1]

The issue was that the `show` method was defined in the `private` section of the controller 🤦.

[^1]: [thoughtbot/clearance - github.com](https://github.com/thoughtbot/clearance)
