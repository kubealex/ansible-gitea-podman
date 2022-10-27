ansible-gitea-podman
=========

This is a quick and dirty role to instantiate a Podman based Gitea [https://gitea.io/en-us/](https://gitea.io/en-us/) instance for dev/test purposes.

Role Variables
--------------
The role has these predefined variables in *defaults/main.yml*:

    gitea_ssh_port: 2222 # Sets up the listening port for SSH on the host
    gitea_web_port: 3000 # Sets up the listening port for Gitea web interface/Registry on the host
    gitea_admin_user: gitea # Admin username
    gitea_admin_password: redhat # Admin password
    gitea_admin_email: gitea@gitea.lab # Admin email

Dependencies
------------

*containers.podman* collection is required to run the module.

Example Playbook
----------------

User this requirements.yml to setup your dependencies:

    ---
    collections:
      - community.general
      - ansible.posix
    roles:
      - name: ansible-gitea-podman
        src: https://github.com/kubealex/ansible-gitea-podman.git

Sample usage with default settings:

    - hosts: podman_host
      roles:
        - ansible-gitea-podman

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
