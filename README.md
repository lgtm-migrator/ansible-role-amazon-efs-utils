# ansible-role-amazon-efs-utils #

[![GitHub Build Status](https://github.com/cisagov/ansible-role-amazon-efs-utils/workflows/build/badge.svg)](https://github.com/cisagov/ansible-role-amazon-efs-utils/actions)
[![Total alerts](https://img.shields.io/lgtm/alerts/g/cisagov/ansible-role-amazon-efs-utils.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/cisagov/ansible-role-amazon-efs-utils/alerts/)
[![Language grade: Python](https://img.shields.io/lgtm/grade/python/g/cisagov/ansible-role-amazon-efs-utils.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/cisagov/ansible-role-amazon-efs-utils/context:python)

This is an Ansible role for installing
[amazon-efs-utils](https://github.com/aws/efs-utils).

## Requirements ##

None.

## Role Variables ##

| Variable | Description | Default | Required |
|----------|-------------|---------|----------|
| create_efs_users_group | Whether or not to create a group for EFS share users. | `true` | No |
| efs_users_gid | The GID to assign the group for EFS share users. | [Omitted](https://docs.ansible.com/ansible/latest/user_guide/playbooks_filters.html#making-variables-optional) | No |
| efs_users_group | The name of group to be created for EFS share users. | `efs_users` | No |
<!--
| required_variable | Describe its purpose. | n/a | Yes |
-->

## Dependencies ##

None.

## Example Playbook ##

Here's how to use it in a playbook:

```yaml
- hosts: all
  become: yes
  become_method: sudo
  roles:
    - amazon-efs-utils
```

## Contributing ##

We welcome contributions!  Please see [`CONTRIBUTING.md`](CONTRIBUTING.md) for
details.

## License ##

This project is in the worldwide [public domain](LICENSE).

This project is in the public domain within the United States, and
copyright and related rights in the work worldwide are waived through
the [CC0 1.0 Universal public domain
dedication](https://creativecommons.org/publicdomain/zero/1.0/).

All contributions to this project will be released under the CC0
dedication. By submitting a pull request, you are agreeing to comply
with this waiver of copyright interest.

## Author Information ##

Shane Frasier - <jeremy.frasier@trio.dhs.gov>
