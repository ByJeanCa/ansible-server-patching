# 🔄 Ansible Server Patching
Simple playbook for updating Linux servers with Ansible.

# # 🚀 How to use
Edit the inventory in inventory/hosts.ini with your servers:
`1.2.3.4 ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa
`  
# # Test connection:
`ansible -i inventory/hosts.ini all -m ping`  

# # Run the patch:
`ansible-playbook -i inventory/hosts.ini server_patch.yml
`  

# # 📦 What it does
* Updates packages (apt or dnf depending on distro) an generates a report.
  
# # 📂 Structure
inventory/            # Inventories  
roles/update_packages # Role with update tasks  
server_patch.yml      # Main playbook


# # #Author: @ByJeanCa
