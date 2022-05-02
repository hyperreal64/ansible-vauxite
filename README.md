# ansible-vauxite

> Experimental playbook aiming to provision [Vauxite](https://github.com/hyperreal64/vauxite) system using Ansible

Install Ansible on Vauxite without rpm-ostree:

```bash
python3 -m ensurepip
python3 -m pip install ansible
ansible --version
```

Playbook runs:

```bash
cd playbooks/
ansible-playbook host.yaml -K
ansible-playbook flatpaks.yaml

# Create and enter a new toolbox
toolbox create
toolbox enter
ansible-playbook toolbox.yaml -K

```
