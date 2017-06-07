* CosmosDB
    *  Features
        * Globally distributed
        * Native PaaS service (multi-tenant)
        * Strong resource governance to prevent noisy-neighbor
        * Cheaper
        * Global replication
    * CosmosDB vs MongoDB API
        *  MongoDB - Been around for 5-10 yrs. 
        * MongoDB is still local
		* Put translation layer on top of core DB layer
        * MongoDB API has quirks
        * Replica set has cost
        * Sharded clusters cost extra nodes
        * Cosmos has Automatic indexing
        * "Aggregation Pipeline" In private preview
            *  https://docs.mongodb.com/manual/core/aggregation-pipeline/
    * vs ATLAS
        * Using MongoDB on a VM underneath
        * Have to do sharding
        * Need machines to manage cluster
    * Support for 3rd party clients (Mongoose)
        * Down the line.  Need more testing
    * Document and graph DB
    * Hourly billing
	* Consistency offerings
        * https://en.wikipedia.org/wiki/CAP_theorem
		* Strong
		* Bounded-stateless (set bound on staleness k-prefix, no staler than 100 writes, or 100ms)
		* Session - each user is guaranteed to read their own write
		* Consistent prefix - Ordering of replication.  If I do writes 1,2,3, all replicated in order of 1,2,3 
		* Eventual
	* Latency
		* 99%-ile single-digit latency
		* Financially backed
* Oracle
    * RAC
        * Not supported in AWS or Azure
    * DataGuard - Disaster Recovery for Oracle DB
    * GoldenGate - Replication Managment for Oracle DB
    * Oracle Express - Just for dev
* SQLServer
    * Lightspeed - https://www.quest.com/products/litespeed-for-sql-server/
        * Fast backup and recovery sol'n
		
	
	
