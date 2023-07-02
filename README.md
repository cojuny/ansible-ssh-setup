# ansible-ssh-setup
Automating transfer of public keypair to a linux ssh remote server, bypassing password prompt in future use.  

### How to use:
1. Install [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) and ansible.posix plugin in your local machine.
   ```shell
   # sudo ansible-galaxy collection install ansible.posix
2. Configure a server (or a virtual server) and remember its ip address, username, and password.
3. Create a ssh key pair.
   ```shell
   # ssh-keygen
5. Change the \<ip-addr-to-server\>, \<username\>, \<location-to-key\> in files inventory and add_public keys.yaml accordingly.
6. Run the scripts:
   ```shell
   # ansible-playbook add_public_keys.yaml -k -K
