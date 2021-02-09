Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = "2048"
    v.cpus = 2
    v.customize ["modifyvm", :id, "--cpuexecutioncap", "70"]
#   v.default_nic_type = "82543GC"
  end
# config.trigger.after :up do |trigger|
#   run "subscription-manager register --username <username> --password <password> --auto-attach
#   trigger.name = "After-Up Trigger ..."
#   trigger.info = "Trigger Execution ..."
#   trigger.run = { path:"subscription-manager register --username <username> --password <password> --auto-attach"}
# end
  config.vm.define "gaussRH7" do |gaussRH7|
    gaussRH7.vm.box = "clouddood/RH7.5_baserepo"
    gaussRH7.vm.hostname = "gaussRH7"
    gaussRH7.vm.network "private_network", ip: "192.168.60.177"
#   gaussRH7.vm.network "private_network", ip: "192.168.60.157", nic_type: "virtio"
    gaussRH7.vm.provision "shell", :inline => "sudo echo '192.168.60.177 gaussRH7.local gaussRH7' >> /etc/hosts"

##  Use Main / Update in Vagrant provision command ### $vagrant provision --provision-with shell/main/update

    # Default
    gaussRH7.vm.provision "main", type: "ansible" do |ansible|
      ansible.playbook = "deploy_gaussRH7_DEV.local.yml"
#     ansible.playbook = "deploy_gaussRH7_DEV.local.yml"
#     ansible.playbook = "deploy_gaussTestRH7.yml"
      ansible.inventory_path = "vagrant_hosts"
      #ansible.tags = ansible_tags
      #ansible.verbose = ansible_verbosity
      #ansible.extra_vars = ansible_extra_vars
      #ansible.limit = ansible_limit
    end
    # Update
#   gaussRH7.vm.provision "update", type: "ansible" do |ansible|
#     ansible.playbook = "deploy_gaussPatchRH7_DEV.local.yml"
#     ansible.playbook = "deploy_gaussTestRH7.yml"
#     ansible.inventory_path = "vagrant_hosts"
#     #ansible.tags = ansible_tags
#     #ansible.verbose = ansible_verbosity
#     #ansible.extra_vars = ansible_extra_vars
#     #ansible.limit = ansible_limit
#   end
  end
# config.trigger.before :destroy do |trigger|
#   run "rm -Rf /tmp/abc/*"
    # subscription-manager remove --all
    # subscription-manager unregister
    # subscription-manager clean
#   trigger.name = "Destroy Trigger ..."
#   trigger.info = "Destroy Trigger Execution ..."
#   trigger.run = { path: "subscription-manager remove --all"}
#   trigger.run = { path: "subscription-manager unregister"}
#   trigger.run = { path: "subscription-manager clean"}
# end
end
