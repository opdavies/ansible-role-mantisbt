# Ansible Role: MantisBT

Installs the [Mantis bug tracker](https://www.mantisbt.org/).

## Requirements

`php` and `mysql` should be installed and working.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    mantis_version: 1.2.19

Which version of Mantis to use.

    mantis_file_extension: tar.gz

The file extension of the archive to use.

    mantis_parent_dir: /var/www

The directory that Mantis will be moved into once extracted.

    mantis_create_db: true
    mantis_install_db: true

Whether to create and/or install the database.

    mantis_remove_admin: true

Whether or not to remove the `admin` directory. This is recommended for security reasons.

    mantis_db_name: mantis
    mantis_db_user: mantis
    mantis_db_pass: mantis

The database credentials to create and connect to the database.

    mantis_admin_username: administrator
    mantis_admin_real_name: ''
    mantis_admin_email: root@localhost
    mantis_admin_password: root

The details for the Mantis admin user.

## Dependencies

None (but PHP and MySQL need to be installed; the `geerlingguy.php` and `geerlingguy.mysql` roles are recommended).

## Example Playbook

    - hosts: all
      roles:
        - opdavies.mantisbt

## Author

[Oliver Davies](https://www.oliverdavies.uk) - PHP Developer and Linux System Administrator.
