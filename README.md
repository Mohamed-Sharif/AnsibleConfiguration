# Ansible Configuration

This repository contains an Ansible playbook that installs and configures Nginx web server on Ubuntu 20.04. 

## Getting Started

To use this playbook, you will need to have Ansible installed on your local machine.

```bash
git clone https://github.com/Mohamed-Sharif/AnsibleConfiguration.git
```

## Usage

To use this playbook, you will need to update the `inventory` file with the IP address of the server that you want to configure. You can do this by running the following command:

```bash
nano inventory
```

Then, replace the IP address in the file with the IP address of your servers.

Next, you can run the playbook with the following command:

```bash
ansible-playbook playbook.yml
```

This will install and configure Nginx on your server.

## Roles

This playbook contains a single role called `web`. The template for this rule was created using the following command:
```bash
ansible-galaxy init web
```
The `web` role installs and configures Nginx on your server. It does the following:

- Installs the Nginx package
- Copies the `index.html` file to the server
- Configures Nginx to serve the `index.html` file
- Restarts the Nginx service

## Testing

To test the playbook, you can use the included `test.yml` playbook. Apply the `playbook.yml` playbook, and then run some basic tests to ensure that Nginx is working correctly.
```bash
ansible-playbook -i inventory test.yml
```
