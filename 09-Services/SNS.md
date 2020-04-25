# What is SNS?

Amazon Simple Notification Service is a service provided by AWS which allows developers to notify users in an immediate, push-based manner.

These notifications can be sent out through a variety of mediums, including email, push notifications to various mobile and desktop clients, SMS, SQS queues and any HTTP endpoint.

## How Does It Work?

SNS uses a concept called "topics", which are essentially subscription lists of users who have subscribed for identical copies of the same notification. A topic can support multiple endpoint types. For example, when you publish once to a topic, your subscribers automatically receive properly formatted copies of a message regarldess of whether they have requested it over email, SMS or push notification.

* All messages published to SNS are stored across multiple availability zones.

## Benefits

* Instant poll-free push-based delivery
* Simple to use API
* Flexible message delivery over a variety of protocols.
* Inexpensive pay-as-you-go model, no upfront costs
* Easy to use web console.

## SNS vs SQS

* Both are messaging systems in AWS
* SQS is poll-based, whereas SNS is push-based