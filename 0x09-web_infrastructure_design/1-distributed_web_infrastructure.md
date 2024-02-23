1. For every additional element, why are adding it:
	Adding a new server so that we can
	be able to add a load balancer to handle too much incoming traffic and also enable us to
	eliminate a single point of failure which could occur by having just one server.

2. What distribution algorithm your load balancer is configured with and how it works:
	Our load balancer uses the Round Robin algorithm which connects in order
	unless a server is down. Requests are served by the server sequentially one after
	another. After sending the request to the last server, it starts from the first server again.
	This algorithm is used when servers are of equal specification and there are not many
	persistent connections.

3. Is your load-balancer enabling an Active-Active or Active-Passive setup, explain
the difference between both: 
	The load balancer enables an Active-Active setup where
	both nodes (servers) are actively running the same kind of service simultaneously. While
	in an Active-Passive setup, not all nodes are going to be active. In the case of two
	nodes, if the first node is already active, the second node must be passive or on standby.
	The key difference between these two architectures is performance. Active-active
	clusters give you access to the resources of all your servers during normal operation. In
	an active-passive cluster, the backup server only sees action during failover.

4. How a database Primary-Replica (Master-Slave) cluster works:
	master-slave
	replication enables data from one database server (the master) to be replicated to
	one or more other database servers (the slaves). The master logs the updates, which
	then ripple through the slaves. If the changes are made to the master and slave at
	the same time, it is synchronous. If changes are queued up and written later, it is
	asynchronous. It is usually used to spread read access on multiple servers for
	scalability, although it can also be used for other purposes such as for failover, or
	analyzing data on the slave in order not to overload the master.

5. What is the difference between the Primary node and the Replica node in regard to
the application:
	A replica node is a copy of the primary node, they provide redundant
	copies of the application codebase to protect against hardware failure and increase
	capacity to serve read requests like searching or retrieving a document
