# collaboration vm
Provides a base Ubuntu 18.04 Vagrant/Virtualbox VM with a second IP on the host's physical network that other users can access.  This allows for rapid iteration on a disposable machine while enabling collaboration with others on the network.  This *WILL NOT* work over VPN.

## Usage

1. General info

This VM differs from other vagrant boxes in that there is an additional NIC that has an IP address others can reach on the physical network.  

*NOTE*: THIS WILL NOT WORK WHEN A VPN IS ACTIVE ON YOUR SYSTEM.

*NOTE2*: The physical network must provide DHCP services for this `Vagrantfile` to work unmodified.  If your network does not, supply static config in the Vagrantfile.

1. Booting up the VM

    `vagrant up`
    
1. To SSH

    `vagrant ssh`

1. Note the IP address others can use to access your VM in the vagrant output:
   ```
   default: Others can access your server at: W.X.Y.Z
   ```