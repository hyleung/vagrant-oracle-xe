Vagrant::Config.run do |config|

  config.vm.define :oraxe do |db1_config|
    db1_config.vm.box = "ubuntu-1110-server-amd64"
    db1_config.vm.box_url = "http://timhuegdon.com/vagrant-boxes/ubuntu-11.10.box"
    db1_config.vm.host_name = "oraxe"
    db1_config.vm.provision :puppet, :module_path => "modules", :options => "--verbose --trace" do |puppet|
      puppet.manifests_path = "manifests"
      puppet.manifest_file  = "site.pp"
    end
    db1_config.vm.customize [ "modifyvm", :id, "--name", "dev_env_oraxe" ,"--memory", "2048"]
  end

end
