# event-sourcing

Problem definitions inspired by: 
https://docs.microsoft.com/en-us/azure/architecture/patterns/event-sourcing

## Microservices:

### Shopping Cart Microservice

Emits following events:

1. an item added to a user cart
1. an item removed from a user cart
1. shipping information updated
1. shipping information removed
1. payment information added
1. payment information removed
1. order placed

### Past Orders Microservice

Returns reverse-chronologically ordered list of orders