# ansible-vauxite

> Experimental playbook aiming to provision [Vauxite](https://github.com/hyperreal64/vauxite) system using Ansible

Install Ansible on Vauxite without rpm-ostree:

```bash
python3 -m ensurepip
python3 -m pip install ansible
ansible --version
```

- Edit `configs/flatpak.yaml`, `configs/toolbox.yaml`, `configs/toolbox_vars.yaml` and `config/host.yaml`
- Run with `ansible-playbook setup.yaml -K`

- Flatpak names are case sensitive. While flatpak is ok with it, creation of symlinks will fail.

- `ansible-playbook setup.yaml --tags flatpak` <- Run only flatpak tasks
- `ansible-playbook setup.yaml --tags toolbox` <- Run only toolbox tasks ( for all toolboxes )
- `ansible-playbook setup.yaml --tags fedora-toolbox-35` <- Run only specific toolbox tasks
- `ansible-playbook setup.yaml --tags host -K` <- Run only host tasks
