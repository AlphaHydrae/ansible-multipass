# Ansible multipass

An ansible role that sets facts to support multi-platform roles.

The following facts will be set when you include this role:

* `host_root_user` - The username of the root user (e.g. `root`).
* `host_root_group` - The group of the root user (e.g. `root`).
* `host_root_home` - The home directory of the root user (e.g. `/root`).
* `host_user_homes` - The base directory where user home directories are located (e.g. `/home`).
* `host_package_manager_paths` - Additional directories to be added to the PATH for the host's package manager (e.g. `/usr/local/bin:` for Homebrew).



## Role Variables

All the following variables have defaults and are optional.

**Generic defaults**

* `multipass_root_user` - The generic name of the root user (defaults to `root`).
* `multipass_root_group` - The generic name of the root group (defaults to `root`).
* `multipass_root_home` - The generic home directory of the root user (defaults to `/root`).
* `multipass_user_homes` - The generic base directory where user home directories are located (defaults to `/home`).

**Darwin-specific defaults**

* `multipass_darwin_root_user` - The name of the root user on Darwin (defaults to `root`).
* `multipass_darwin_root_group` - The name of the root group on Darwin (defaults to `wheel`).
* `multipass_darwin_root_home` - The home directory of the root user on Darwin (defaults to `/var/root`).
* `multipass_darwin_user_homes` - The base directory where user home directories are located on Darwin (defaults to `/Users`).

**Homebrew-specific defaults**

* `multipass_homebrew_paths` - Additional directories to add to the PATH for Homebrew (defaults to `/usr/local/bin:`).

**MacPorts-specific defaults**

* `multipass_macports_paths` - Additional directories to add to the PATH for MacPorts (defaults to `/opt/local/bin:/opt/local/sbin:`).



## Example Playbook

    - hosts: servers
      roles:
         - { role: AlphaHydrae.multipass }
