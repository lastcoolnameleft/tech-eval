* Docker
    * Tools
        * Docker Image - Snapshot of a container
        * Docker Container - A running instance of a Docker Image
        * Docker Engine - Creates and runs containers (aka Docker Daemon)
        * Docker Compose - Tool for defining and running multi-container Docker apps
            * Uses docker-compose.yml
        * Docker Client - CLI to interact with Engine via REST
        * Docker Hub - SaaS Docker Image Repository
        * Docker Cloud - Hosted management service
            * Manage: builds, images, swarms, infrastructure, nodes, registry
        * Docker Datacenter - Creates CaaS platform from on-premesis
        * Docker for Mac - Easy to install native, Docker Development Env.
            * Uses macOS Hypervisor framework, networking and filesys
            * Supercedes Docker Toolbox
        * Docker for Windows - Easy to install native, Docker Development Env.
            * Works with Win10 + Win Serv 2016, Uses MSFT Hyper-V
            * Supercedes Docker Toolbox
        * Docker Enterprise Edition (EE) - Platform and Support for Enterprise solutions
            * Includes Docker Trusted Registry, Docker Datacenter, security framework
            * https://docs.docker.com/enterprise/
        * Docker Registry - Docker image repository
        * Docker Store - Store for Trusted Docker images
        * Docker Swarm Mode - Standalone clustering tool
            * Pools docker hosts and exposes as one
            * Very confusing naming convention
        * Docker Machine - CLI tool for managing hosts with Docker Engine
    * Legacy
        * Swarm - Cluster Mgmt + orchestrator
            * Replaced by Docker Swarm Mode
            * Very confusing naming convention
        * Docker Toolbox - Installs Docker Engine, Docker Compose, Docker Machine, Kitematic 
            * Replaced by Docker for Win/Mac
        * boot2docker - lighteight Linux distro for Mac & Win
            * Replaced by Docker-machine
        * Kitematic - GUI for managing Containers
* Kubernetes - Container Orchestrator
    * Terms
        * Pod
            * building block
            * Usually one container on a host (could be more; rare)
            * Gets unique IP addr
        * Job
            * Runs till completion
            * Job name must be unique
* Helm
    * Concept:
        * Chart - Package to run
        * Tiller
* Rancher - http://rancher.com/
    * Container Mgmt/Orchestrator Deployment
	* Not OSS
	* Tried deploying "mgmt host" on Azure.  Failed
        * Saw resources (Vnet, storage, IP, etc.) deployed
        * 5 minutes later, all gone, but storage acc't
    * Similar to Azure Container Service
    * Application Catalog -> similar to Helm
* Draft - https://github.com/Azure/draft
    * Tool for developers to create apps for K8S
    * Currently only for K8S
    * By Deis/Microsoft
	* Best walkthrough: https://www.noelbundick.com/2017/05/31/Draft-on-Azure-Container-Service/
	* Definitely smooth for getting your code into a cluster
	* Requires working K8S cluster.
        * Doesn't really work on desktop/laptop (yet)
        * Minikube doesn't work
	* Archives and ships app dir to draftd service to containerize and publish to ACR
    * Save file -> Get new prod env (~15-30 sec) Strange delay even after pushing and refreshing
* Flannel - https://github.com/coreos/flannel
    * Network fabric for containers, designed for K8S
    * By CoreOS
    * Gives a subnet to each host for use with container runtimes
* Source-to-image - https://github.com/openshift/source-to-image
	* Builds docker images from source
    * Kinda like Draft, but a lot less features
        * doesn't auto-upload
* Forge - http://forge.sh/
    * Kinda like draft, but less features.
		* Upload project to k8s cluster
		* Instead of “forge deploy”, Draft watches your project to upload
        * Draft also doesn’t require an extra manifest file.
* Dump-Init - https://github.com/Yelp/dumb-init
    * minimal init system for Linux containers
* Istio - platform-independent service mesh
    * https://istio.io
    * Initially for K8S (uses sidecars)
    * Connect, Manage and Secure Microservices
    * Features
        * Traffic management
            * Config Route Request - route based upon src, dest, header, and/or cookie
            * Used for A/B Testing, Canary Releases, Staged Rollouts with % split
        * Fault injection - Add delay to request to see how system responds
        * Telemetry collection - Graphana + Dotviz/graph
        * Circuit Breaker - Limit upon max connections
        * Policy enforcement
* Flannel - L2 network fabric for containers, designed for Kubernetes
    * https://github.com/coreos/flannel#flannel
    * virtual network that gives a subnet to each host for use with container runtimes
        * Kubernetes assume that each container (pod) has a unique, routable IP inside the cluster
        * this reduces the complexity of doing port mapping
* Calico - L3 container networking provider and network policy engine
    * https://www.projectcalico.org//
    * provides network policy solution for connecting Kubernetes pods
    * can be deployed without encapsulation or overlays. 
    * provides security policy for Kubernetes pods via its distributed firewall.
    * can also be run in policy enforcement mode in conjunction with other networking solutions such as Flannel, aka canal
    * https://www.projectcalico.org/demo
* Canal - Composition of calico and flannel plugins
    * Policy based networking for cloud native applications
    * https://github.com/projectcalico/canal
    * allow users to easily deploy Calico and flannel networking together as a unified networking solution
* Aqua - Container Security Company
    * Image Assurance
    * Thread Mitigation
    * Runtime Profile
    * Container Firewall
    * User access control
* Minikube - Run K8S locally
    * runs a single-node Kubernetes cluster inside a VM on your laptop
    * https://kubernetes.io/docs/getting-started-guides/minikube/
* OpenShift - Enterprise Kubernetes
    * Adds tools on top of Kubernetes
    * By Redhat
    * OpenShift Origin - OSS version of OpenShift
        * Not recommended for production
        * Same binaries at OCP, but ahead of OCP (stable)
    * Openshift Online - multi-tenant cloud-based container platform, managed by RH
    * Openshift Online - single-tenant cloud-based container platform, managed by RH
    * Openshift Container Platform - 
        * 3-4 months behind
    * Concepts
        * Bastion Node
        * Infra Nodes
        * Application Nodes
        * Master Nodes
    * Openshift.io - CI/CD Platform 
* Kubespray - Deploys a K8S Cluster
    * Can deploy to AWS, GCE, Azure, OpenStack or Baremetal
    * https://github.com/kubernetes-incubator/kubespray
* Heapster - Compute Resource Usage Analysis and Monitoring of Container Clusters
* Docker-sync - Sync files to docker containers for dev
    * http://docker-sync.io/
    * Boilerplate setup:  https://github.com/EugenMayer/docker-sync-boilerplate
* cAdvisor - Analyzes resource usage and performance characteristics of running containers.
    * Container Advisor - By Google
* Inspector - Kubernetes pod inspector
    * https://github.com/kelseyhightower/inspector/
* Portworx - Container Storage solution
    * Pooled & s/w defined
    * Storage virtualization - serves virtual volumes
    * Features: Backup, Snapshots
    * Container focused
        * Deploys as containers
        * Docker volume driver
        * Scheduler aware
        * per-volume encryption
        * If scheduler moves container, volume moves with it
    * Lighthouse - UI
        * Need Reverse Proxy for accessibility
    * Similar to GlusterFSa
* K8 Guard - https://github.com/k8guard/
    * Audit system for K8S
* Ark - https://github.com/heptio/ark
    * Manages K8S disaster recovery for cluster resources and persistent volumes