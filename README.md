# PAM
Сreate users and add restrictions to them

### Задача:

Ограничить доступ к системе для всех пользователей, кроме группы
администраторов, в выходные дни (суббота и воскресенье), за исключением
праздничных дней.

### Решение:


#### создадим ВМ согласно Vagrantfile:

mkdir /home/maria/homework/my_vagrant_pam

cd /home/maria/homework/my_vagrant_pam

touch Vagrantfile

#### создадим Ansible-playbook, inventory

mkdir /home/maria/homework/my_vagrant_pam/ansible

cd /home/maria/homework/my_vagrant_pam/ansible

touch provision.yml

touch hosts

#### запуск

vagrant up

#### проверка

ssh otus@192.168.56.22

ssh otusadm@192.168.56.22
