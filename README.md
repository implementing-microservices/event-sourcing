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

Listens to following events:

1. ms-payment.payment-processed

### Payment Processing Microservice (ms-payment)

Emits following events:

1. `Payment Processed`. Data elements:
    - cart_id
2. `Payment Failed`
    - cart_id

### Past Orders Microservice

Listens to events from Shopping Cart to create query-able, materialized view. Returns reverse-chronologically ordered list of orders
