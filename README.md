Install and configure Portainer
=========

The role installs and configures Portainer for my server.

Role Variables
--------------

A list of the variables that need to be set can be seen below

Example Playbook
----------------

```yaml
- hosts: servers
  vars:
    portainer_root_domain: example.com

    portainer_notifications:
      smtp_username: ""
      smtp_password: ""
      smtp_host: ""

    portainer_authelia:
      jwt_secret: ""
      session_secret: ""
      storage_secret: ""
      user_name: ""
      user_password: ""
      user_email: ""
      display_name: ""

    portainer_cloudflare_api_key: ""

    portainer_grafana:
      admin_user: admin
      admin_password: ""

    portainer_influxdb:
      password: ""
      secret: ""

    portainer_passbolt:
      mariadb_root_password: ""
      mariadb_database_password: ""
      description: ""
      user_email: ""
      user_surname: ""
      user_name: ""

    portainer_dashy:
      description: ""

    portainer_authelia_config_template_path: templates/authelia-config.yaml.j2
    portainer_dashy_config_template_path: templates/dashy-conf.yaml.j2

  roles:
      - role: tychobrouwer.docker
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
