# Create deploy user

## Installation

1. Add servers IP or FQDN to inventory file such as inventory/inventory.cfg (see inventory/inventory.cfg.sample)
2. Add SSH publickey to files directory for setup key-based authentication
3. Add variables to host_vars or group_vars (see host_vars/0.0.0.1/)
4. Run make create-deploy-user
