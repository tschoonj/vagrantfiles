## Script to generate a working Vagrant CentOS 8 box

1. Install [VirtualBox](https://www.virtualbox.org). Available from [Homebrew](https://brew.sh): `brew cask install virtualbox`
2. Install [Vagrant](https://www.vagrantup.com). Also available from [Homebrew](https://brew.sh): `brew cask install vagrant`
3. Install [ansible](https://www.ansible.com). Via [Homebrew](https) this would be: `brew install ansible`
4. Execute `vagrant up` to launch the VM and start the provisioning (time to drink/eat something).
5. By default this VM will launch without GUI (this can be changed in the Vagrantfile), so you will need to run `vagrant ssh` to access it.
6. Run `vagrant halt` to shut the VM down.

