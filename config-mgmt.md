* Cloud-init - https://cloudinit.readthedocs.io/en/latest/
    * Great for Ubuntu, but very good in Centos
    * Doesn't have capability/flexibility as Ansible
	* Cisco standardizes on Centos (Not RHEL) Marketplace
* Habitat - https://www.habitat.sh/
    * Centalized Configuration Manager 
    * "Make quick config changes"
    * Personal review:  I don't get it.  Appears to be a passthru for env vars.  You could add env vars via a file, which was neat, but underwhelming
* Consul 
    * By Hasicorp:
    * Features: key/value store, health checking, service discovery
    * Similar to etcd & zookeeper, but does service discovery
* Packer
    * By Hashicorp
    * Create identical machine images for multiple platforms from single config
    * EC2, Azure, Docker, Google Compute Engine, OSTK, QEMU (Both KVM & Xen), VirtualBox, VMWare