# Simple Workflow Service

[Amazon SWF](https://aws.amazon.com/swf/) or Simple Workflow Service is used to manage task-based workflows.

* Amazon SWF ensures that a task is assigned only once and is never duplicated.
* Amazon SWF keeps track of all tasks and events in an application. This is unlike SQS, in which it is typically necessary to implement your own application-level tracking especially if your application uses multiple message queues.

## Components of SWF

* **Workflow starters** - an application that can initiate a workflow. Examples include an e-commerce site following the placement of an order by a human user, or a mobile app searching for bus times.
* **Deciders** - control the flow of activity tasks in a workflow execution. If something has finished (or failed) in a workflow, a Decider decides what to do next.
* **Activity workers** - Carry out the activity tasks.