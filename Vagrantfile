$curl = <<-SCRIPT 
sudo apt-get install curl -y && sudo apt-get clean
SCRIPT
$docker = <<-SCRIPT
curl -fsSL https://get.docker.com | bash
SCRIPT
Vagrant.configure("2") do |config|
config.vm.box = "ubuntu/trusty64"
config.vm.define "et-01" do |et01|
    et01.vm.provision "shell", inline: $curl
    et01.vm.provision "shell", inline: $docker
    et01.vm.network "public_network", bridge: "en1: Wi-Fi (AirPort)"
end
config.vm.define "et-02" do |et02|
    et02.vm.provision "shell", inline: $curl
    et02.vm.provision "shell", inline: $docker
    et02.vm.network "public_network", bridge: "en1: Wi-Fi (AirPort)"
end
config.vm.define "et-03" do |et03|
    et03.vm.provision "shell", inline: $curl
    et03.vm.provision "shell", inline: $docker
    et03.vm.network "public_network", bridge: "en1: Wi-Fi (AirPort)"
end
end
