DESCRIPTION

Playbook to install debian on a system from a live image. Code is very raw and only useful for educationnal purpose. Ansible was only used for readability and organisation (few ansible modules were actually used, its mostly used as a shell wrapper).

HOW TO USE

- Boot a debian 12 live environment and connect to internet
- Install ansible and git on the live environment
```
sudo apt install ansible git
```
- Clone this repo to the live env
```
git clone https://github.com/parmoli/ansible_debian_install
```
- Edit vars.yml to setup varibles
```
nano ansible_debian_install/vars.yml
```
- Edit main.yml to comment unecessary tasks
```
nano ansible_debian_install/main.yml
```  
- Run the playbook (with sudo for chroot connexions)
```
sudo ansible-playbook ansible_debian_install/main.yml
```

TODO

- Setup /var/log and @flatpak btrfs subvolumes
- Implement disk encryption options
- Make systemd-boot an option (?)
- Some tasks files are unfinished/empty ...
- ...
