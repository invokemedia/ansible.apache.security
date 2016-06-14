# Ansible Role: Apache Security

A simple Ansible Role to enable the common security flags for apache Server Signature and Server Tokens ofr Apache 2.x on Debian/Ubuntu.

## Role Variables

  apache_server_signature: "Off"

View the [ServerSignature Directive](https://httpd.apache.org/docs/2.4/mod/core.html#serversignature) on the Apache docs for more information.

  apache_server_token: "Prod"

View the [ServerTokens Directive](https://httpd.apache.org/docs/2.4/mod/core.html#servertokens) on the Apache docs for more information.

## Dependencies

This role depends on the geerlingguy.apache role.

## Example Playbook

  - hosts: webservers
    vars_files:
      - vars/main.yml
    roles:
      - { role: invoke.apache.security }

*Inside `vars/main.yml`*:

  apache_server_signature: "Off"
  apache_server_tokens: "Prod"

## License

MIT / BSD

## Author Information

This role was created in 2016 by [Invoke Media](https://www.invokemedia.com)
