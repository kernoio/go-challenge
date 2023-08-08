# Senior Go Backend Challenge

## Setup

Clone this project, it contains a docker-compose file. It already has a service from which you
will receive messages to complete this challenge.

## Challenge

Write a little message aggregator service (wsclient) that:

- Connects via websocket to `wsserver` (provided). On connection, the server will send you:
  1. A list of parent / child associations (with uuid's)
  2. Messages representing the status of communications between services, where the `source` and `destination` attributes are UUID's corresponding to a `child`.
  3. Every now and then it will send a new list of parent/child associations (it's an update not a replacement).  
- The client you write should:
  - every 1 minute deliver back to the server (through the same connection) a **count()** aggregation with `{from,to, count}` fields **grouped by parent UUID** 

## Message types
ParentChildAssociation
```[{"parent":"36de4bf4-0293-4567-b009-75c4bc66a64d","child":"4b68f084-c3f1-4b7d-860d-7c68bbbbaa51"}, ...]```

Message
```{"source":"e7924178-0132-4730-9c79-89fed571567f","destination":"f3f83156-2ad0-45fa-938f-591e477a1743","method":"GET","path":"/list","httpStatus":400}```

## Considerations
Do consider this is for us to see the way you think and the quality of your code. Think of it as your application letter.

We will be evaluating program architecture, data structures, synchronization, resiliency, resource usage and performance strategies.

## Delivery

Zip the solution and send it (or a download link) to dev-challenges@kerno.io