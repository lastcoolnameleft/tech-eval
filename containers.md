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
    * Initially for K8S
    * Provides traffic management, policy enforcement, and telemetry collection.
    * Connect, Manage and Secure Microservices
    * Demo:  Tried to get working, but his issue setting up RBAC:
        * Step 4, workaround didn't work:
            * https://istio.io/docs/tasks/installing-istio.html
