## Web Network: High Performance


critical components that dictate the performance of all network:

* Latency

    The time from the source sending a packet to the destination receiving it



* Bandwidth 

    Maximum throughput of a logical or physical communication path


The point is take a message, or a packet, to travel from its point of origin
to the point of destination. Typical the router component is responsible for relaying a message between the client and the
server.

* Propagation delay

    Amount of time required for a message to travel from the sender to receiver, which
is a function of distance over speed with which the signal propagates.


* Transmission delay

    Amount of time required to push all the packet’s bits into the link, which is a function of the packet’s length and data rate of the link.


* Processing delay

    Amount of time required to process the packet header, check for bit-level errors,
and determine the packet’s destination.


* Queuing delay

    Amount of time the incoming packet is waiting in the queue until it can be processed.

The total latency between the client and the server is the sum of all the delays just listed.

