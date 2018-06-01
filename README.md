[![Build Status](https://travis-ci.com/mako-ai/ansible-role-facebook-messenger.svg?branch=master)](https://travis-ci.com/mako-ai/ansible-role-facebook-messenger)

This repository contains an Ansible role for creating Facebook test users to test Messenger bots.

## Motivation

Facebook for Developers enables users to create test applications and test users. Manually creating and destroying new test users becomes challenging to maintain, is time-consuming, and impedes the development of Messenger bots.

The purpose of this role is to provide the functionality for creating and configuring test users to be able to message the bot.

Below are some use cases for using this role:

- Quality assurance (QA) testing
- Integrate into existing build and deployment pipelines
- Reusability across different environments (e.g., review, staging, production)

## Example

```yaml
---

- hosts: all
  remote_user: root
  roles:
    - ansible-role-facebook-messenger
  vars:
    graph_subscription_callback_url: http://localhost/facebook/receive

```

## Variables

**Page Variables**

- `graph_page_about`
- `graph_page_category_enum`
- `graph_page_cover_photo_url`
- `graph_page_name`
- `graph_page_picture`

**Subscription Variables**

- `graph_subscription_callback_url`
- `graph_subscription_fields`
- `graph_subscription_object`

**User Variables**

- `graph_user_permissions`
