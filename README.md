DESCRIPTION

Playbook to install debian on a disk from a live image. The code is very raw and only useful for educational purpose. Ansible was only used for readability and organisation (few Ansible modules were actually used, it's mostly used as a shell wrapper).

HOW TO USE

- Boot a debian 12 live environment and connect to the internet
- Install Ansible and git on the live environment
```
sudo apt install ansible git
```
- Clone this repo to the live env
```
git clone https://github.com/parmoli/ansible_debian_install
cd ansible_debian_install
```
- Edit vars.yml to setup variables
```
nano vars.yml
```
- Edit main.yml to comment unnecessary tasks
```
nano main.yml
```  
- Run the playbook (with sudo for chroot connexions)
```
sudo ansible-playbook main.yml
```

TODO

- Setup /var/log and @flatpak btrfs subvolumes
- Implement disk encryption options
- Make systemd-boot an option (?)
- Some tasks files are unfinished/empty ...
- ...
