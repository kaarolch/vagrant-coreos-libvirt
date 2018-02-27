# vagrant-coreos-libvirt

Small Ansible playbook that automate build of vagrant coreos image with libvit provider support.

# Why

Just for fun ;)
I would like to have a stable coreos vagrant image with libvirt, that could be use with [kubespray](https://github.com/kubernetes-incubator/kubespray) to setup home k8s cluster.

My image you can find here: [vagrant-cloud](https://app.vagrantup.com/kaarolch). Yes, there are only image with libvirt support.

# Why you upload private key to the repo?

[vagrant.pem](vagrant.pem) is a public accessible key provided by the hashicorp. You can use your own key. More [here](https://www.vagrantup.com/docs/vagrantfile/ssh_settings.html)

# Image customization

* add vgrant user with sudo password-less rule
* import pub key to allow login without password

# How to run

```
 ansible-playbook main.yml  -K -vvv --extra-vars " vagrant_cloud_user=PUT_YOUR_LOGIN, vagrant_cloud_token=PUT_YOUR_KEY"

```

# To Do
* Add steps to automate upload image to the Vagrant Cloud (90% done).
* Add bootstrap steps to verify if all required component are installed in system.
* Add travis or jenkins file to automate build steps with new version of coreos (to support auto build process)
