* Selinux (Security-Enhanced Linux) - Linux Kernel security module
    * Provides mandatory access controls (MAC) into subsystems of kernel.
* Systemd - Linux init system (like sysv or BSD init), RHEL7
* cssh - Cluster SSH
    * https://github.com/duncs/clusterssh
    * Run single command on multiple servers
    * iTerm version
        * https://github.com/wouterdebie/i2cssh
* Busybox - Minimal Unix OS
    * www.busybox.net
    * 2.1 MB
* DRBD (Distributed Replicated Block Device) - replicated storage sol'n
    * Mirrors content of block devices (hd partitions, LV, etc.) b/w hosts
    * Mirrors data in real time, transparently, async/sync
* Corosync - Cluster Engine
    * The Corosync Cluster Engine is a Group Communication System 
    * Implementing high availability within applications
    * C Application Programming Interface features:
        * A closed process group communication model with virtual synchrony guarantees for creating replicated state machines.
        * A simple availability manager that restarts the application process when it has failed.
        * A configuration and statistics in-memory database that provide the ability to set, retrieve, and receive change notifications of information.
        * A quorum system that notifies applications when quorum is achieved or lost.
    * Pacemaker is built on-top of Corosync
* Pacemaker - storm daemon designed to process heartbeats from workers
    * simple in-memory key/value store with ZooKeeper-like, directory-style keys and byte array values.
    * Apache Project
