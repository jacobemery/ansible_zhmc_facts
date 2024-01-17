# lpar-usage-facts
- Define `hmc_host` and `hmc_user` variables in inventory.yaml
- Define `vault_hmc_pass` variable in vault.yaml
- Set an Ansible vault password in .password.txt
- Encrypt Ansible vault with:
```
ansible-vault encrypt vault.yaml
```
- Run the Ansible Playbook with:
```
ansible-playbook lpar-usage-facts.yaml
```
- Open the created file `output.txt` to see the results.
- Optionally, add verbosity to the playbook command to print the output table to the terminal:
```
ansible-playbook lpar-usage-facts.yaml -v
```