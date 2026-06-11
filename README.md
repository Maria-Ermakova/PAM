# PAM
Сreate users and add restrictions to them

#### создадим ВМ согласно Vagrantfile:

mkdir /home/maria/homework/my_vagrant_pam

cd /home/maria/homework/my_vagrant_pam

touch Vagrantfile

#### создадим Ansible-playbook, inventory

mkdir /home/maria/homework/my_vagrant_pam/ansible

cd /home/maria/homework/my_vagrant_pam/ansible

touch provision.yml

touch hosts

vagrant up

ssh otus@192.168.56.22

ssh otusadm@192.168.56.22
