## Script to generate a working Vagrant vanilla macOS High Sierra box

1. Install [VirtualBox](https://www.virtualbox.org). Available from [Homebrew](https://brew.sh): `brew cask install virtualbox`
2. Install [Vagrant](https://www.vagrantup.com). Also available from [Homebrew](https://brew.sh): `brew cask install vagrant`
3. Install [macinbox](https://github.com/bacongravy/macinbox).
4. Download the High Sierra Installer from the Mac App Store.
5. Modify the following command to your liking and execute (and wait...):

```
sudo macinbox --box-format virtualbox --name high-sierra -m 8192 --installer /Applications/Install\ macOS\ High\ Sierra.app --no-fullscreen
```
6. Execute `vagrant up` to launch the VM
7. By default this VM will launch without GUI (this can be changed in the Vagrantfile), so you will need to run `vagrant ssh` to access it.
8. Run `vagrant halt` to shut the VM down.


