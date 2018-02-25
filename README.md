# vagrant-coreos-libvirt

Small Ansible playbook that automate build of vagrant coreos image with libvit provider support.

# Why

Just for fun ;)
I would like to have a stable coreos vagrant image with libvirt, that could be use with [kubespray](https://github.com/kubernetes-incubator/kubespray) to setup home k8s cluster.

# Why you upload private key to the repo?

[vagrant.pem](vagrant.pem) is a public accessible key provided by the hashicorp. You can use your own key. More [here](https://www.vagrantup.com/docs/vagrantfile/ssh_settings.html) 

# Image customization

* add vgrant user with sudo password-less rule
* import pub key to allow login without password

# To Do
* Add steps to automate upload image to the Vagrant Cloud (90% done).
* Add bootstrap steps to verify if all required component are installed in system.
* Add travis or jenkins file to automate build steps with new version of coreos (to support auto build process)
