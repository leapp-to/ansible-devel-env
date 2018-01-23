# ansible-dev-env
Currently, Leapp project is divided into multiple sub projects. This means that in order to setup a development environment one has to setup everything piece by piece. At this point those pieces are:

* [Snactor library](https://github.com/leapp-to/snactor)
* [Leapp daemon](https://github.com/leapp-to/leapp-go)
* [Leapp tool](https://github.com/leapp-to/leapp) (which includes Cockpit UI plugin)
* [Leapp control tool](https://github.com/leapp-to/leappctl)
* [Leapp actor repository](https://github.com/leapp-to/leapp-actors)

Because we realize that this can be quite complicated and a rather tedious process to be done manually, we prepared this Ansible playbook to setup a development environment for Leapp.

**Currently this Ansible Playbook does support Fedora and CentOS systems**

Follow the steps bellow to set Leapp development environment on your local machine.

```sh
# Make sure you have both Git and Ansible installed
$ sudo dnf install -y git ansible
$ git clone https://github.com/leapp-to/ansible-devel-env.git
$ cd ansible-devel-env/ansible
$ ansible-playbook leapp_dev.yml -K
```
