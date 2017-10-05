* Cloud-init - https://cloudinit.readthedocs.io/en/latest/
    * Great for Ubuntu, but very good in Centos
    * Doesn't have capability/flexibility as Ansible
	* Cisco standardizes on Centos (Not RHEL) Marketplace
* Habitat - Application Build Automation
    * https://www.habitat.sh/
    * By Chef
    * Centalized Configuration Manager 
    * "Make quick config changes"
    * Personal review:  I don't get it.  Appears to be a passthru for env vars.  You could add env vars via a file, which was neat, but underwhelming
    * Containers:
        * Focus on App first and then builds OS that only has what you need
    * Concept:
        * Plan (Bash/Powershell)
        * Artifact
            * HART file which has everything needed to run
        * Depo
        * Supervisor - runs apps
        * Packaging Format - makes apps
        * Supervisor Ring - (e.g. 3 MySQL instances electing a leader)
* Consul 
    * By Hasicorp:
    * Features: key/value store, health checking, service discovery
    * Similar to etcd & zookeeper, but does service discovery
* Packer
    * By Hashicorp
    * Create identical machine images for multiple platforms from single config
    * EC2, Azure, Docker, Google Compute Engine, OSTK, QEMU (Both KVM & Xen), VirtualBox, VMWare
* Terraform
    * By Hashicorp
    * Uses own format to define resources to then upload to provider
    * Can "plan" file before uploading to preview changes
    * After planning config, apply to commit
    * Azure
        * Walkthrough: https://blogs.msdn.microsoft.com/eugene/2016/11/03/creating-azure-resources-with-terraform/
        * If deploy failed, usually easier to delete resource group and try again
        * Some feature gaps for Azure
            * Monitoring Alerts do not work
* Bitbucket - OnPrem Git Server
    * https://www.atlassian.com/software/bitbucket/server
    * By Atlassian
* Ansible - OSS Automation Platform
    * Competitors: Puppet, Chef
    * Functions: Config Mgmt, App Deployment, Task Automation
    * Tower: GUI for CLI
    * Concept:
        * Playbook: declarative file to configure host
* Cloudforms - Manage container, virtual, private, and public cloud infrastructures
    * Manager of managers
    * https://www.redhat.com/en/technologies/management/cloudforms
    * Aggregate from other services (AWS, Azure, etc)
* Bosh - Desired State Management
    * https://bosh.io/
    * From Cloud Foundry
    * release engineering, deployment, lifecycle management, and monitoring of distributed systems
* Open Service Broker API
    * Started by Pivotal
    * Standard way of connecting apps (Stateful and Stateless apps)
* Gogs - self-hosted Git service
    * https://gogs.io/
    * Language: Go
* Jenkins - OSS CI tool
* Spinnaker - OSS CD tool
    * By Netflix
* Fabric8 - Development Pipeline platform for K8S
    * Build, test, deploy containers with approval blocking
    * Feels like Spinnaker for containers
    * Components
        * Config Map Controller - Controls configs of
        * Expose Controller - Resp. for mapping of services b/w Fabric8. Can communicate b/w services with domain names
            * If on Azure, don't forget to change service type to Load Balancer
        * Fabric8 - Glue
        * Fabric8 Force - Scaffolding
        * Gogs, Jenkins, Nexus (Docker Registry)
    * https://github.com/chrisvugrinec/azure-fabric8-with-acsonk8
* Screwdriver - OSS CD Tool
    * By Yahoo
    * https://github.com/screwdriver-cd/screwdriver
* Wildfly - CI platform by Redhat