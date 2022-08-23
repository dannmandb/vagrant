Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/kinetic64"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
 #   ansible.install_mode = "pip_args_only"
#    ansible.pip_args = "-r /vagrant/requirements.txt"
  end

end
