# Personal study notes

## SQS
<details>
<summary>SNS vs SQS ? </summary>
<pre>
- SNS send messages to subscribers through push mechanism
- SQS is queue messaging , means you need to periodically poll
- SQS let you decouple sending and receiving components
</pre>
</details>

<details>
<summary>Why Amazon MQ exists so ?</summary>
<pre>
Just to offer an easy migration from on-premise uses of Apache MQ or Rabbit MQ
If your build new app or ready to refactor all your code go SQS (lol)
</pre>
</details>

<details>
<summary>Does SQS provide ordering and guarantee delivery of messages</summary>
<pre>
- Yes if you use FIFO queue mode
- FIFO queue provide exactly-one processing (each message delivered once and remain available until comsumed)
- Standard mode provides at-least-once delivery, but you have to add sequence info to guarantee order in this mode
</pre>
</details>

<details>
<summary>SQS vs Kinesis streams ? </summary>
<pre>
- SQS for your microservice rock star dev apps
- Kinesis for your scientific business rock star nerd-scientist apps
</pre>
</details>

<details>
<summary>SQS free tier </summary>
<pre>
- 1 million requests per month
- Free usage does not accumulate across months
</pre>
</details>


<details>
<summary>How does Amazon SQS handle messages that can't be processed ? </summary>
<pre>
- dead letter queues (you need to configure it yourself)
</pre>
</details>

<details>
<summary> What is a visibility timeout? </summary>
<pre>
 period of time during which Amazon SQS prevents other consumers from receiving and processing the message
 point is : you are in a distributed system, you can't be sure that consumer will get the message, so you don't want the message to be deleted and/or used by another consumer until the initial consumer actually gets it

- (default, min, max) = (30sec, 0sec, 12h)
</pre>
</details>

<details>
<summary> Does Amazon SQS support message metadata? </summary>
<pre>
 Yes, up to 10 metadata attributes in name-type-value triple forms
</pre>
</details>

<details>
<summary> How can I determine the time-in-queue value? </summary>
<pre>
 request SentTimeStamp attributes and do the maths
</pre>
</details>

<details>
<summary> What is the typical latency for Amazon SQS? </summary>
<pre>
SendMessage, ReceiveMessage, DeleteMessage API requests ~ 100 ms
</pre>
</details>

<details>
<summary> For anonymous access, what is the value of the SenderId attribute for a message? </summary>
<pre>
IP address of the sender (lol)
</pre>
</details>
<details>

<summary> What is Amazon SQS long polling? </summary>
<pre>
helps you reduce the amount of empty messages by allowing Amazon SQS to wait until a message is available in a queue before sending a response
happens when you set a  WaitTimeSeconds for ReceiveMessage API > 0
or when ReceiveMessageWaitTimeSeconds queue attributes > 0 (and caller does not set WaitTimeSeconds in his call)
max long polling wait time = 20sec
</pre>
</details>

<details>
<summary> What is the throughput quota for an Amazon SQS FIFO queue? </summary>
<pre>
By default, FIFO queues support up to 3,000 messages per second with batching or up to 300 messages per second (300 send, receive, or delete operations per second) without batching
</pre>
</details>

<details>
<summary> Why are there separate ReceiveMessage and DeleteMessage operations?  </summary>
<pre>
 You're responsible for deleting the message and the deletion request acknowledges that you’re done processing the message
 If you don’t delete the message, Amazon SQS will deliver it again on when it receives another receive request
</pre>
</details>

<details>
<summary> What happens if I issue a DeleteMessage request on a previously-deleted message?  </summary>
<pre>
 When you issue a DeleteMessage request on a previously-deleted message, Amazon SQS returns a success response.
</pre>
</details>