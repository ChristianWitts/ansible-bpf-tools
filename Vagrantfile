# -*- mode: ruby -*-
# vi: set ft=ruby :
@ansible_home = "/home/vagrant/roles"

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.define :molecule do |molecule_config|
        molecule_config.vm.box = "geerlingguy/centos7"
        # molecule_config.vm.synced_folder ".", "#{@ansible_home}/bpf-tools", type: 'rsync'
        molecule_config.vm.hostname = "molecule.molecule.home"
        molecule_config.vm.network "public_network"
        # Pre-run setup and configuration
        # molecule_config.vm.provision "shell", path: "configure_node.sh"
        molecule_config.vm.provision "shell",
            inline: "cp -pr /vagrant/* /home/vagrant/roles && chown -R vagrant:vagrant /home/vagrant/roles"
        # Run the ansible playbook
        molecule_config.vm.provision "ansible_local" do |ansible|
            ansible.playbook = "#{@ansible_home}/tasks/main.yml"
        end
        config.vm.provider "virtualbox" do |v|
            v.memory = 4096
            v.cpus = 2
        end
    end
end
