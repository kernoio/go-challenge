# Senior Go Backend Challenge

## Setup

Pull a GitHub project, it will contain a docker-compose which has different tools already setup for you to use.
The project is already added and running on docker-compose, but feel free to modify anything you feel it's necessary. 

## Challenge

We want you to develop a message aggregator service.

- You will connect via websocket to a server which will:
  - Send a first message with a list of parent services and its children
  ```[{"parent":"36de4bf4-0293-4567-b009-75c4bc66a64d","child":"4b68f084-c3f1-4b7d-860d-7c68bbbbaa51"}, ...]```
  - Send messages every 1 second with communications done between the children, these UUID are always at children level
  ```{"source":"e7924178-0132-4730-9c79-89fed571567f","destination":"f3f83156-2ad0-45fa-938f-591e477a1743","method":"GET","path":"/list","httpStatus":400}```
  - Now and then it will send a list of new parent and children that need to be added to the current one
- The client should aggregate messages every 1 minute and send them back:
  - We want to see here how many times a service has talked to another one during that minute
  - The aggregation must be done at parent level
  - For this you'll need to use the received child uuid and search to which parent it belongs

## Considerations

- Challenge must be done on Go
- You are free to structure the projects, choose frameworks and/or libraries as you see fit to deliver on this project. 
- Feel free to use any of the infrastructure pieces provided in the docker-compose file or add your own choices to it. It does have to work with a simple `docker-compose up` tho.
- We will be evaluating data structures, synchronization, resiliency, resource usage and performance strategies.
- Feel free to ask any question if there is something it's not clear

## Nice to have

If you have extra time, or you consider these are important

- Tests
- Commits order and messages
- Validations
- Logs
- Error management

## Delivery

Do not create a PR, as it's a shared repo, it will be deleted asap.
Zip the project upload it to any file manager and send the link by email