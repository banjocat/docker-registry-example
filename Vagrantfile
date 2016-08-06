Vagrant.configure("2") do |config|

    config.vm.box_url = "ubuntu/xenial64"
    config.vm.box = "ubuntu/xenial64"


    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook_vagrant.yml"
    end

    config.vm.define "docker" do |docker|
        docker.vm.network "public_network"
        docker.vm.hostname = "everythingisawesome.com"
    end

end
