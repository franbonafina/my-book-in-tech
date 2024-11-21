## Event-Driven in Google Cloud:

* Event Source: Identify the source of events, such as Pub/Sub, Cloud Storage, or HTTP requests.

* Event Trigger: Configure Cloud Run services to be triggered by these events.

* Event Processing: Design your Cloud Run service to process the event data, perform transformations, or trigger subsequent actions.


### Workflow Automation:

* Step-by-Step Processes: Break down your workflow into smaller, discrete steps.

* Service Orchestration: Use Cloud Run services to execute each step, either sequentially or in parallel.

* Error Handling and Retries: Implement mechanisms to handle failures and retry failed steps.


### Scalability/Reliability

* Auto-scaling: handle workloads auto-scaling config **)


* Redundacy: deploy multiple instance to ensure high-availability **)


* Monitoring and Logging: implement robust monitoring, logging to track performance and identify issues.


### Building Blocks:

* The event processing package should be on Docker containers.

* Use Http, cloud-storage or Pub/Sub for trigger initiate services

* Config Environments


### Pub/Sub

* 
