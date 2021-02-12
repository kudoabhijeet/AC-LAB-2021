# Experiment 2: Working with Vagrant

## Steps Performed

### Installing VirtualBox
 - First install VirtualBox in order to run vagrant.
    `sudo apt-get update`
    `sudo apt install virtualbox`

### Installing Vagrant  
 - Download Vagrant.
    `curl -O https://releases.hashicorp.com/vagrant/2.2.9/vagrant_2.2.9_x86_64.deb`

- Install Vagrant `sudo apt install ./vagrant_2.2.9_x86_64.deb`

- Verify install `vagrant --version`
![I1](https://user-images.githubusercontent.com/46739435/107741911-1734df00-6d34-11eb-9317-f3315b5d21c9.png)

- Create a directory `mkdir LAB1`, change directory `cd LAB1` and initialize vagrant `vagrant init`.
![I1](https://user-images.githubusercontent.com/46739435/107741911-1734df00-6d34-11eb-9317-f3315b5d21c9.png)

- Vagrantfile would be created. Open Vagrantfile `vim Vagrantfile`
![I2](https://user-images.githubusercontent.com/46739435/107741915-18660c00-6d34-11eb-954c-685685e9c527.png)



- Change variable `config.vm.box = "ubuntu/xenial64"`
![Screenshot from 2021-02-12 13-21-55](https://user-images.githubusercontent.com/46739435/107742584-4f88ed00-6d35-11eb-933a-ed3a3e9753b3.png)

- Use `vagrant up` to run vagrant.
![I3](https://user-images.githubusercontent.com/46739435/107741918-18fea280-6d34-11eb-949f-d54cebaf1abe.png)

- New machine would be created in VirtualBox
![I4](https://user-images.githubusercontent.com/46739435/107741919-19973900-6d34-11eb-9bcf-9965087ebac3.png)

- Perform various operations in vagrant.
- Use `vagrant halt` to shutdown vagrant.
- Use `vagrant destroy` to destroy machine.
![I5](https://user-images.githubusercontent.com/46739435/107741922-1ac86600-6d34-11eb-80ff-f96068e97377.png)
