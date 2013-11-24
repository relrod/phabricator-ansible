Vagrant.configure("2") do |config|
  config.vm.box = "CentOS-6.4-x86_64"
  config.vm.box_url = "http://developer.nrel.gov/downloads/vagrant-boxes/CentOS-6.4-x86_64-v20130427.box"

  config.vm.define :phabricator, primary: true do |phabricator|
    phabricator.vm.network :private_network, ip: "192.168.111.99"

    phabricator.vm.provider :virtualbox do |v|
    v.name = "phabricator"
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--memory", 512]
    v.customize ["modifyvm", :id, "--cpus", 1]
    v.customize ["modifyvm", :id, "--name", "Phabricator"]
    end

    phabricator.vm.provision :ansible do |ansible|
      ansible.inventory_path = "rhel6/hosts"
      ansible.playbook = "rhel6/site.yml"
    end
  end
end
