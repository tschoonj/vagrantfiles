## Script to generate a working Vagrant macOS High Sierra box with Xcode, Command Line Tools and MacPorts

1. Install [VirtualBox](https://www.virtualbox.org). Available from [Homebrew](https://brew.sh): `brew cask install virtualbox`
2. Install [Vagrant](https://www.vagrantup.com). Also available from [Homebrew](https://brew.sh): `brew cask install vagrant`
3. Install [macinbox](https://github.com/bacongravy/macinbox).
4. Download the High Sierra Installer from the Mac App Store.
5. Modify the following command to your liking and execute (and wait...):

```
sudo macinbox --box-format virtualbox --name high-sierra -m 8192 --installer /Applications/Install\ macOS\ High\ Sierra.app --no-fullscreen
```
6. Install [ansible](https://www.ansible.com). Via [Homebrew](https) this would be: `brew install ansible`
7. Download Xcode 10.1 (for High Sierra) and the Command Line Tools for Xcode 10.1 from the [Apple Developer website](https://developer.apple.com): this is free, but you will need to create an account with them.
8. But both these files (they should be named `Command_Line_Tools_macOS_10.13_for_Xcode_10.1.dmg` and `Xcode_10.1.xip`) into the `provisioning/files` folder.
9. Execute `vagrant up` to launch the VM and start the provisioning (time to drink/eat something).
10. By default this VM will launch without GUI (this can be changed in the Vagrantfile), so you will need to run `vagrant ssh` to access it.
11. Run `vagrant halt` to shut the VM down.

Note: the ansible roles were taken from the [Ansible Galaxy](https://galaxy.ansible.com/home), but were (heavily) modified as they were not properly working, or doing what I wanted them to...

