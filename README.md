# Senior Go Backend Challenge

## Setup

Pull a GitHub project, it will contain a docker-compose which has different tools already setup for you to use.
The project is already added and running on docker-compose, but feel free to modify anything you feel it's necessary. 

## Challenge

We want you to develop a message aggregator service.

- It will connect via websocket to a server which will send messages every 1 second
- The client should aggregate messages every 1 minute and send them back.
- Messages will be a list of requests done between many services and we'd like to know how many times during that minute a service has hit another one.
- As a plus we'd like you to consider adding extra information on the message as part of the protocol, like if the message needs ack, message id, type and encoding.
    - You don't need to implement ack or encoding, we only want you to add this information as part of the protocol.
    - The server won't respond anything, so you can define it as you consider it's the best solution.

## Considerations

- Challenge must be done on Go
- We don't want you to spend more than 2/3hs on it
- Quality > Quantity, meaning we rather to see a good architectured solution and well written code than a fully working solution
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