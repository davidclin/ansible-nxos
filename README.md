# ansible-nxos
These are sample playbooks for Cisco NXOS using examples of NX-API/CLI transports and common tasks that are useful to invoke show/config commands.

These playbooks utilize an nxapi and cli provider for authentication.

Example providers used for these playbooks are:

# /etc/ansible/group_vars/all.yaml
nxos_nxapi_connection:
  host: "{{ inventory_hostname }}"
  username: admin
  password: "#cisco123"
  transport: nxapi
  use_ssl: no
  validate_certs: no

nxos_cli_connection:
  host: "{{ inventory_hostname }}"
  username: admin
  password: "#cisco123"
  transport: cli
  
# tree structure starting from /etc/ansible
nxos.yml
nxos_clean.yml
hosts 
group_vars/
└── all.yml

# sample hosts file
[n9k]
10.1.1.1
10.1.1.2
etc
