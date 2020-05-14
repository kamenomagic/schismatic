---
layout: page
title: Rails
---

## Get a key from credentials based on environment
* `Rails.application.credentials[(ENV['KEY_ENVIRONMENT'] || Rails.env).to_sym][:example][:secret_key]`

## Create a new project, with familiar options
* `rails new project-name-here --api --database=postgresql`

## Create user postgres
* `Create user USER with password 'password';`
* `ALTER USER username CREATEDB;`