# proxmox-deploy-vm-ansible-ubnt2204
Deploy Ubuntu 22.04 VM from  Template in Proxmox

To start the playbook you must:

1. Fill in the data (variables) in the file vars/vars.yaml

2. Add ssh key to proxmox

3. Check inventory file

4. Run the command in the terminal

Fill in the data (variables) in the file vars/vars.yaml

```yaml
  vmID: {id} (free virtual machine ID) !!!
  hostname: {hostname} (vm hostname and option name)
  cores: {n} (count of vcores)
  memory: {1024*n} (megabytes) 
  eth: {}
  ip: {ip/mask} (ip address with net mask)
  gateway: {gw_ip} (default gateway ip address)
```

Set Users passwords
```yaml
 sadmin_pasw: {password} (just password)
  root_pasw: {password} (just password)  
```

Run playbook:
```yaml
ansible-playbook -i inventory createVm-playbook.yaml
```
