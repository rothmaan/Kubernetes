Vagrant.configure("2") do |config|

     NodeCount = 1

     (1..NodeCount).each do |i|
       config.vm.define "k8s" do |k8s|
         k8s.vm.box = "ubuntu/bionic64"
         k8s.disksize.size = "20GB"
  #       k8s.vm.network "private_network", ip: "192.168.1.50"
         k8s.vm.hostname = "k8s.example.com"
         #k8s.vm.hostname = "k8s#{i}.example.com"
         k8s.vm.provider "virtualbox" do |v|
           v.memory = 6000
           v.cpus = 2
  #         v.gui = true
           #config.vm.provision "shell", path: "scripts/setup_ssh.sh"
           config.vm.provision "shell", inline: <<-SHELL
           sudo apt-get update -y
           sudo apt-get install software-properties-common -y
           sudo apt-add-repository --yes --update ppa:ansible/ansible
           sudo apt-get install ansible --yes
           sudo gpasswd -a vagrant lxd
           SHELL
           end
        end
     end
 end
