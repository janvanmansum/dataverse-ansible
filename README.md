# Dataverse Ansible role

This [Ansible][ansible] role aims to install [Dataverse][dataverse] and its prerequisites.
The role installs PostgreSQL 9.3, GlassFish 4.1 and other prerequisites, then deploys Dataverse 4.2.1
into GlassFish.

## Usage:
	$ ansible-playbook -i <inventory file> [-u <user>] [-s] [-K] -e @<group_vars_file> [-v] dataverse.yaml

The role currently supports CentOS 7 with all services running on the same machine, but hopes to become OS-agnostic and support multiple nodes for scalability.

If you're interested in testing Dataverse locally using [Vagrant][vagrant], you'll want to clone this repository and edit the local port redirects if the http/https ports on your local machine are already in use. Note that the current Vagrant VM template requires [VirtualBox][virtualbox] 5.0.

### To test using Vagrant:
	$ git clone https://github.com/IQSS/dataverse-ansible
	$ cd dataverse-ansible
	$ vagrant up

This is a community effort, only distantly supported by [IQSS][iqss]. The role is under active development - pull requests, suggestions and other contributions are welcome!

[ansible]: http://ansible.com
[dataverse]: https://dataverse.org
[iqss]: http://www.iq.harvard.edu
[vagrant]: https://www.vagrantup.com
[virtualbox]: https://www.virtualbox.org
