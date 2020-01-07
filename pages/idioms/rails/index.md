---
layout: page
title: Rails
---

## Get a key from credentials based on environment
* `Rails.application.credentials[(ENV['KEY_ENVIRONMENT'] || Rails.env).to_sym][:example][:secret_key]`
