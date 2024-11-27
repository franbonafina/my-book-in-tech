*  Parsing and serializing large JSON objects can be computationally expensive.


* Software engineering is always a game of tradeoffs. Because something is in fashion doesn’t make it universally right for all problems and use cases.
What matters is knowing about the different architectural options, understanding
their pros and cons, and, importantly, understanding the requirements and needs of
your own problem. (And, yes, in some cases and situations, having a monolith is OK.)


* The difference between 
(functions vs. serverless containers) is just the degree to which developers want to shift the
boundaries of shared responsibilities. Containers give you a bit more control over
user space libraries and network capabilities.



* Events-driven API design
```
      "1. **Event Publication:**": {
        "API Endpoint": "POST /events",
        "Description": "Expose an endpoint for publishing events to a central event bus or notification system.",
        "Request Example": {
          "body": {
            "eventType": "order.created",
            "eventId": "12345",
            "timestamp": "2024-11-21T12:00:00Z",
            "payload": {
              "orderId": "56789",
              "customerId": "112233",
              "items": [
                {
                  "productId": "A1",
                  "quantity": 2
                }
              ]
            }
          }
        },
        "Response Example": {
          "status": 202,
          "message": "Event accepted for processing."
        }
      },
      "2. **Event Subscription:**": {
        "API Endpoint": "POST /subscriptions",
        "Description": "Allow components to subscribe to specific events by registering their endpoints.",
        "Request Example": {
          "body": {
            "subscriberId": "service-A",
            "eventTypes": ["order.created", "order.updated"],
            "callbackUrl": "https://service-a.example.com/webhooks"
          }
        },
        "Response Example": {
          "status": 201,
          "subscriptionId": "sub-98765"
        }
      },
      "3. **Event Delivery (Webhooks):**": {
        "Event Example": {
          "headers": {
            "X-Event-Type": "order.created",
            "X-Event-Id": "12345"
          },
          "body": {
            "orderId": "56789",
            "customerId": "112233",
            "items": [
              {
                "productId": "A1",
                "quantity": 2
              }
            ]
          }
        },
        "Retry Mechanism": "Use exponential backoff for retries if the subscriber endpoint fails to acknowledge the event."
      },
      "4. **Event Querying:**": {
        "API Endpoint": "GET /events/{eventId}",
        "Description": "Provide an endpoint to fetch event details for debugging or auditing purposes.",
        "Response Example": {
          "status": 200,
          "body": {
            "eventType": "order.created",
            "eventId": "12345",
            "timestamp": "2024-11-21T12:00:00Z",
            "payload": {
              "orderId": "56789",
              "customerId": "112233",
              "items": [
                {
                  "productId": "A1",
                  "quantity": 2
                }
              ]
            }
          }
        }
      }
    }
```



* Devops Movement CAMS: Culture, Automation, Measurement and Sharing.

* 