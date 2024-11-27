# Lambda

Lambda costs are based on:
* The number of invocations
* The hundreds of milliseconds of execution time of all invocations,
depending on the memory given to the functions.
* When a function terminates, no session
information is retained.
  (This kind of interaction with a server is usually defined
as stateless)
* Serverless means: no management infra, scale-out of the box and pay-as-you-use