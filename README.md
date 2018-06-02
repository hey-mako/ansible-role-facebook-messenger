> Ansible role for creating Facebook test users to test Messenger bots.

[![Build Status](https://travis-ci.com/mako-ai/ansible-role-facebook-messenger.svg?branch=master)](https://travis-ci.com/mako-ai/ansible-role-facebook-messenger)

## Motivation

[Facebook for Developers](https://developers.facebook.com/) enables users to create test applications and test users. Manually creating and destroying new test users becomes challenging to maintain, is time-consuming, and impedes the development of Messenger bots.

The purpose of this role is to provide the functionality for creating and configuring test users to be able to message the bot.

Below are some use cases for using this role:

- Quality assurance (QA) testing
- Integrate into existing build and deployment pipelines
- Reusability across different environments (e.g., review, staging, production)

## Install

    $ ansible-galaxy install mako-ai.facebook-messenger

## Dependencies

This role does not have any dependencies.

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

| Name                         | Type  | Required                 |
|------------------------------|------ |:------------------------:|
| `graph_page_about`           | `str` | :heavy_multiplication_x: |
| `graph_page_category_enum`   | `str` | :heavy_multiplication_x: |
| `graph_page_cover_photo_url` | `str` | :heavy_multiplication_x: |
| `graph_page_name`            | `str` | :heavy_multiplication_x: |
| `graph_page_picture`         | `str` | :heavy_multiplication_x: |

**Subscription Variables**

| Name                              | Type  | Required                 |
|-----------------------------------|-------|:------------------------:|
| `graph_subscription_callback_url` | `str` | :heavy_check_mark:       |
| `graph_subscription_fields`       | `seq` | :heavy_multiplication_x: |
| `graph_subscription_object`       | `str` | :heavy_multiplication_x: |

**User Variables**

| Name                     | Type  | Required                 |
|--------------------------|-------|:------------------------:|
| `graph_user_permissions` | `seq` | :heavy_multiplication_x: |

## License

MIT © [Mako AI](https://github.com/mako-ai)
