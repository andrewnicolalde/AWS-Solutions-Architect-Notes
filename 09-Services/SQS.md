# What is SQS?

[Amazon SQS](https://aws.amazon.com/sqs/), or simple queue service is a message cue available om Amazon AWS. It facilitates message delivery between different components of an application.

## Use cases

* Useful in applications which need in-order delivery of messages (see FIFO queue)
* Useful in applications in which different components may be intermittently connected to the network.
* Useful in applications in which the loss of messsages is unacceptable

## Types of SQS Queues

1. **Standard Queue**
    * Nearly unlimited number of transactions per second
    * Best-effort message ordering
    * Message duplication is possible
2. **FIFO Queue**
    * Exactly-once processing
    * Guaranteed in-order message delivery
    * Limited to 300 messages per second, but have all other capabilities of standard queues

## Exam Tips

* SQS is pull-based (NO PUSH NOTIFICATIONS)
* SQS guarantees your messages will be processed **at least once**
* Messages are limited to 256 KB in size, though apparently it is possible to have larger messages which are actually stored in S3 (look into this)
* Messages can be kept in the queue configurably between 1 minute and 14 days. The default message retention time is 4 days.
* **Visibility Timeout** - the length of time for which a message is invisible to the queue after a reader picks up the message. If the message is not processed within the visibility timeout window it could be picked up by another reader and therefore be delivered twice.
    * If you're finding that many messages are being delivered twice, your visibility timeout likely is not large enough as even normal processing times are apparently larger than the timeout.
    * The max visibility timeout is 12 hours.
* **Long Polling** - long polling is a way to retrieve messages from SQS queues. While short polling returns immediately even if there is nothing in the queue, long polling doesn't return a response until something arrives in the queue or until the long poll times out.
  * This is useful because each poll of the SQS queue incurs a charge.
* Any scenario-based question where you see "decoupling" mentioned, SQS is almost certainly the answer.