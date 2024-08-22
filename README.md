# ansible-ids
Repository with Ansible project to build IDS sensors using Zeek and Suricata on Ubuntu 22.04 or 24.04

You can clone this repository, modify a couple of files and be up and running in a few minutes.

Edit inventory/hosts with the IPs or hostnames of your target IDS hosts.

You'll need to remove the encrypted version of inventory/group_vars/ids/vault, rename vault.unencrypted to vault, edit the file with your own settings, then re-encrypt the vault with 'ansible-vault encrypt vault' with the passkey of your choice.

With those steps done, from the root of the folder you cloned/downloaded the project to, run 'ansible-playbook playbooks/site.yml --ask-vault-pass' and provide the vault passkey you set before.
