___NOTICE___ - *Under active development*

## ABOUT

Ansible modules to support Cisco NX-OS network build automation use-cases.  Developed for Ansible 1.5.  This library is not currently part of the Ansible distribution.  Please refer to [INSTALLATION](#installation) section for setup.

For examples of using this module library, refer to the [Ansible Autozone](https://github.com/Mierdin/ansible-autozone) demo repository.

## OVERVIEW OF MODULES

This library contains the following Ansible modules.  For detailed usage on each module, refer to [docs](docs).

#### Build Automation modules

These are the primary modules used to install Junos OS softawre and deploy the initial configuration.  These modules only require that the NX-OS device(s) accept SSH connections. In the future, the NX-OS XML interface may be used as well.

* `nxos_install_rawconfig` - Install a raw NX-OS configuraiton

#### Utility modules

* `nxos_shutdown` - Perform a 'shutdown' or 'reboot' command

## INSTALLATION

Coming soon!

## DEPENDENCIES

These modules require the following to be installed on the Ansible server (more requirements to be added later):

* [Ansible](http://www.ansible.com) 1.5 or later
