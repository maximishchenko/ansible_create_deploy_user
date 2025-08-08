# Create deploy user

Playbook 

- Install minimal required packages (sudo)
- Create user for deployment with pre-defined password
- Append user to sudo group
- Add SSH-key for key-based authentication

## Preparation

1. Add servers IP or FQDN to inventory file such as ```inventory/inventory.cfg```

> Example [inventory/inventory.cfg.sample](inventory/inventory.cfg.sample))


2. Add SSH publickey to [files](files/) directory for setup key-based authentication with name ```agent_rsa.pub```

> Example

```shell
cp ~/.ssh/id_rsa.pub files/agent_rsa.pub
```

3. Add variables to host_vars or group_vars

> Example [host_vars/0.0.0.1/](host_vars/0.0.0.1))

## Usage

1. Run with ```Makefile```:

```shell
make setup
```

or your can pass path to inventory file with environment variable

```shell
make setup INVENTORY=inventory/my_inventory_file.cfg
```

2. Run Ansible Playbook directly

```shell
ansible-playbook -i inventory/inventory.cfg create_deploy_user.yml
```
