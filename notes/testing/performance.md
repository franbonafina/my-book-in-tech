## Performance Testing
Following are key indicators that must be
taken into account to provide us with an accurate idea of how an application is performing and its impact. 

### Service-oriented
They measure how well (or not) an application is providing a service to the end users. 

* *Availability*:

    The amount of time an application is available to the end user. Lack of availability is
    significant because many applications will have a substantial business cost for even a small
    outage. In performance testing terms, this would mean the complete inability of an end
    user to make effective use of the application.


* *Response-time:*

    The amount of time it takes for the application to respond to a user request. For
    performance testing, one normally measures system response time, which is the time
    between the user’s requesting a response from the application and a complete reply
    arriving at the user’s workstation.

### Efficiency-oriented 
They measure how well (or not) an application makes use of the
application landscape.

* *Throughput*

    The rate at which application-oriented events occur. A good example would be the
    number of hits on a web page within a given period of time.


* *Utilization*

    The percentage of the theoretical capacity of a resource that is being used. Examples
    include how much network bandwidth is being consumed by application traffic and the
    amount of memory used on a server when a thousand visitors are active.


## Performance Standard



| Response Time         | User Experience                                                                                 |
|-----------------------|-------------------------------------------------------------------------------------------------|
| 15 seconds            | Rules out conversational interaction. May be acceptable for simple inquiries, but not for busy users.            |
| 4-15 seconds          | Delays are too long for conversations requiring short-term memory retention. May be acceptable after transaction completion. |
| 2-4 seconds           | Inhibiting for operations requiring high concentration. May be acceptable after minor closure.                   |
| Less than 2 seconds   | Necessary for applications requiring information retention throughout multiple responses.                         |
| Subsecond response time | Required for thought-intensive work, such as writing or graphics-rich applications.                             |
| Deci-second response time | Almost instantaneous response required for interactive applications, such as computer games.                 |


