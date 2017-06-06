* Apache Nifi  - https://nifi.apache.org/
    * Enterprise Dataflow
	* Concepts:
		* Interactive command and control
		* Data lineage
		* Platform build for extension
		* flow based programming
	* Architecture
		* Each nifi node runs in JVM on node(VM)
		* All interactions via webserver
		* Flow controller - exec task
		* FlowFile - Metadata about tasks in flow (like headers of HTTP)
		* Conent Repo - the meat
		* Provenance Repo - tracability, don't want RPC to 3rd party.  Massaging data constantly
	* Can choose batching properties by saying "we can accept 25ms delay to promote micro-batching"
	* A lot more than messaging
	* "Simple event processing" - discrete obj and you can do soemthing about it
		* Vs complex event processing (time window obj, looking at series of obj at once and making assertion)
			§ Spark/Storm are built to do that.
	* Why build?
		* Messaging didn't address full problem
		* Want to see how data is flowing
		* Make immediate changes
        * Not dev->test->prod changes