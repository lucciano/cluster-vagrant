http://www.beegfs.com/wiki/ManualInstallWalkThrough

Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"

  config.vm.define "web" do |web|
    web.vm.box = "ubuntu/vivid64"
  end

  config.vm.define "db" do |db|
    db.vm.box = "ubuntu/vivid64"
  end
end
