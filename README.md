# Formation_Libre

## Liferay Skeleton
This project contains an Ansible playbook to set up a Liferay Portal server. It can either be used to set up a test, stage, production or any other environment, as well as provisioning a Vagrant VM for development purposes.

Setup/provisioning includes the installation of a Liferay Portal server and its prerequisites:

a MySQL database
a Java 11 JDK
a Liferay 7.2 Tomcat bundle.

## Starting and using the VM
See Vagrant Documentation how to work with Vagrant. Important commands are:

vagrant up
vagrant provision
vagrant halt
vagrant destroy

## Using the VM
After the VM is successfully started and provisioned, open http://localhost:8080/ in a browser and follow the requested steps. Sign in with the default admin user:

a Email Address: test@liferay.com
a Password: test

## Server setup with Ansible
The Ansible playbook, that is used to provision the Vagrant VM, can also be used to set up the Liferay system (including MySQL and Java) on other environments (servers), too. For each additional environment, an inventory file ansible/inventory/[environment] has to be created. Replicate an existing inventory file and adjust its contents regarding to the new environment and/or see the documentation on the Ansible home page: Ansible Docs - Inventory. If the new environment requires custom configurations, create a file ansible/host_vars/[environment].yml and configure the variables that should be overwritten.

To run the setup call:

ansible-playbook ansible/playbook.yml \
                 -i ansible/inventory/[environment]

## Variables for Liferay version
The default variables define the (currently) latest version of the Liferay Portal server for installation. If a server should be set up with another version, those variables can be overwritten, e.g. in the regarding ansible/host_vars/[environment].yml file for the server to be set up. Prefedined variables for known versions can be found in the directory ansible/roles/liferay/vars/versions and can simply be overwritten in the ansible/host_vars/[environment].yml file.

#### Les environnements

    - Développement
    - Production
