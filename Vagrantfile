ENV[‘VAGRANT_SERVER_URL’] = ‘https://vagrant.elab.pro’

Vagrant.configure(“2”) do |config|

  # отключение синхронизации автоматически создаваемой общей папки между
хостом и ВМ

  #config.vm.synced_folder “.”, “/vagrant”, disabled: true

  config.vm.define “PAM” do |server|

  server.vm.box = ‘ubuntu/22.04’

  server.vm.host_name = ‘PAM’

  #Host-Only Network

  server.vm.network :private_network, ip: “192.168.56.22”

  server.vm.provider “virtualbox” do |vb|

  vb.memory = “1024”

  vb.cpus = “1”

  end

  server.vm.provision “ansible” do |ansible|

  ansible.playbook = “ansible/provision.yml”

  ansible.inventory_path = “ansible/hosts”

  #отключение проверки SSH ключей, необходимо для тестирования в
безопасной изолированной среде

  ansible.host_key_checking = false

  end

  end

end
