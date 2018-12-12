Vagrant.configure(2) do |config|
  config.vm.box = "jacqinthebox/windowsserver2016"
  config.vm.guest = :windows
  config.vm.communicator = "winrm"
  #config.vm.network :forwarded_port, guest: 3389, host: 3389
  #config.vm.network :forwarded_port, guest: 5985, host: 5985, id: "winrm", auto_correct: true
  config.vm.network :public_network
  config.vm.synced_folder "C:\\Usersdbat\\source\\repos\\MyBookStore", "/vagrant"

  config.vm.provider "virtualbox" do |vagrantTest|
    vagrantTest.gui = true
    vagrantTest.memory = 2048
  end

  config.vm.provision "shell", path: "iis_setup.ps1", privileged: true

end