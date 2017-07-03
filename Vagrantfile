Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.define "wazuh" do |wazuh|
  end

  config.vm.provider "virtualbox" do |v|
    v.linked_clone = true
  end

  config.vm.provision "shell",
    :path => "vagrant_specs.sh",
    :upload_path => "/home/ubuntu/specs",
    # change role name below
    :args => "--install ansible-wazuh-server"
end
