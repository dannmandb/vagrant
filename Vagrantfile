# -*- mode: ruby -*- 
# vi: set ft=ruby : 

VAGRANTFILE_API_VERSION = "2" 

Vagrant.configure(VAGRANTFILE_API_VERSION) do|config| 
    config.ssh.insert_key = false 
    config.vm.provider :virtualbox do|vb| 
        vb.customize ["modifyvm", :id, "--memory", "2048"] 
    end 
    
    #Web Server 
    config.vm.define "web1" do|web| 
        web.vm.hostname = "web-server" 
        web.vm.box = "ubuntu/kinetic64" 
        web.vm.network "public_network", ip: "192.168.1.210" 
    end 
    
    #Application Server1 
    config.vm.define "app1" do|app| 
        app.vm.hostname = "app-server1" 
        app.vm.box = "ubuntu/kinetic64" 
        app.vm.network "public_network", ip: "192.168.1.211" 
    end 
    
    #Application Server2 
    config.vm.define "app2" do|app| 
        app.vm.hostname = "app-server2" 
        app.vm.box = "ubuntu/kinetic64" 
        app.vm.network "public_network", ip: "192.168.1.212" 
    end 
    
    #Database Server 
    config.vm.define "db" do|db| 
        db.vm.hostname = "database-server" 
        db.vm.box = "ubuntu/kinetic64" 
        db.vm.network "public_network", ip: "192.168.1.213" 
    end 
    
    config.vm.box_check_update = false 
    config.vbguest.auto_update = false 
end
