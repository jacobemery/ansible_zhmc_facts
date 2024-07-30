# lpar-usage-facts
Example playbooks for demonstrating Ansible's ability to gather facts from the Hardware Management Console (HMC) using the [ibm.ibm_zhmc](https://galaxy.ansible.com/ui/repo/published/ibm/ibm_zhmc/) collection.

How To:
Pre-Requisites:
- Access and permissions to a Hardware Management Console (HMC).
- Ansible and Python installed on the Ansible Controller
- ibm.ibm_zhmc collection installed
```
ansible-galaxy collection install ibm.ibm_zhmc
```

How To:
- Set an Ansible Vault password in .password.txt
- Change permissions for .password.txt to be accessible only to you.
```
chmod 600 .password.txt
```
- Define variables in inventory.yml
- For hmc_auth.password, use ansible-vault to encrypt the string
```
ansible-vault encrypt_string
```
- When prompted, enter the HMC password, press Ctrl+D twice to finish.
- Copy the output from ansible-vault directly starting from "!vault |" all the way to the end of the string of numbers.
- Paste the encrypted password into inventory.yml after the colon for hmc_password value.
- Finish entering in variables for inventory.yml
- Run playbooks
```
ansible-playbook all_zhmc_facts.yml
```
