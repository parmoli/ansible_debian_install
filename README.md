DESCRIPTION

Playbook to install debian on a system from a live image. Code is very raw and only useful for educationnal purpose. Ansible was only used for readability and organisation (few ansible modules were actually used, its mostly used as a shell wrapper).

HOW TO USE

- boot a debian 12 live environment and connect to internet
- install ansible and git on the live environment
sudo apt install ansible git
- clone this repo to the live env
git clone https://github.com/parmoli/ansible_debian_install
- edit ansible_debian_install/vars.yml to setup varibles
- edit ansible_debian_install/main.yml to comment unecessary tasks
- launch the playbook (with sudo for chroot connexions)
sudo ansible-playbook ansible_debian_install/main.yml

TODO

- setup /var/log and @flatpak btrfs subvolumes
- implement disk encryption options
- make systemd-boot an option (?)
- some tasks are unfinished or empty (?)
- ...
