Vagrant.configure("2") do |config|

    config.vm.box_url = "ubuntu/xenial64"
    config.vm.box = "ubuntu/xenial64"

    # Only needed cause of bug in vagrantfile for xenial
    config.vm.provider "virtualbox" do |vb|
        vb.name = "docker-registery"
    end

    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook.yml"
    end

    config.vm.define "docker" do |docker|
        docker.vm.hostname = "everythingisawesome.com"
        config.vm.network "private_network", type: "dhcp"
    end

end


