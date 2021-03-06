---
id: jdbc-outbound-gateway
title: JDBC outbound gateway
sidebar_label: JDBC outbound gateway
---
#### Sends messages to a database and/or receives messages using an SQL query.
<a href="http://docs.spring.io/spring-integration/docs/2.2.x/reference/html/jdbc.html#jdbc-outbound-gateway" target="_blank">External documentation</a>

Defines an outbound gateway for updating a database in response to a message on the request channel, and/or for retrieving data from the database using the input message as a source of parameters for the specified SQL select query.

The database response will be used to create the response message on the reply channel.

The response can be created from a query supplied here, or (if <i>keys generated</i> is <code>true</code>) can be the primary keys generated from an auto-increment, or else just a count of the number of rows affected by the update.  The response is in general a case insensitive map (or list of maps if multi-valued), unless a select query and a row-mapper is provided.  If the update count is returned then the map key is <code>"UPDATE"</code>.

#### SQL data source
Reference to a JDBC data source, usually including some form of connection pooling, used for accessing the database.

<i>Required</i>

#### Update query
An UPDATE query to be executed when a message is received. If this is in a transaction then the update will roll back when the transaction does.

An UPDATE query is required, unless a SELECT query is specified. If you specify both UPDATE and SELECT query, then the UPDATE is executed first.

Note that you can use the message payload and headers from the request message as parameters in the query by using the colon prefix notation.

Example of a query using header and payload values from the request message:
<code>INSERT INTO mytable (id, createddate, contents) values (:headers[id], :headers[timestamp], :payload)</code>

#### Select query
A SELECT query to execute when a message is received. The result of this query will be the body of the outgoing message.

The query can return multiple rows; if you want to convert rows in the SELECT query result to individual messages you can use a downstream splitter.

Note that you can use the message payload and headers from the request message as parameters in the query by using the colon prefix notation.

Example of a query using header values from the request message:
<code>SELECT * FROM mytable WHERE id = :headers[id]</code>

Be aware that when settings <i>keys generated</i> to <code>true</code>, the root of the colon prefix notation expression will be the generated keys (a map if there is only one or a list of maps if multi-valued) and not the request message.

<i>Optional</i>

#### Maximum rows per poll
When using a SELECT query, you can set a custom limit regarding the number of rows extracted into the outgoing message.

Default only the first row is extracted. If set to <code>0</code> all rows are extracted.

<i>Optional</i>

#### Keys generated
Flag to indicate whether primary keys are generated by the query. 

If they are then they can be used as a reply payload instead of providing a SELECT query. A single valued result is extracted before returning (the usual case), so the payload of the reply message can be a Map (column name to value) or a list of maps.

Default is <code>false</code>.

#### Requires reply
Specify whether this outbound gateway must return a non-<code>null</code> value, i.e. whether every request message must result in a reply message.

If <code>true</code>, a <code>ReplyRequiredException</code> will be thrown when the underlying service returns a <code>null</code> value.

Default is <code>true</code>.

#### Reply timeout
Allows you to specify how long (in milliseconds) this gateway will wait for the reply message to be sent successfully to the reply channel before throwing an exception. This attribute only applies when the channel might block, for example when using a bounded queue channel that is currently full.

Also, keep in mind that when sending to a <i>direct channel</i>, the invocation will occur in the sender's thread. Therefore, the failing of the send operation may be caused by other components further downstream.

If not specified, by default the gateway will wait indefinitely.

#### Request channel
Channel to consume the request messages from.

<i>Required</i>

#### Reply channel
Channel where reply messages should be sent to.

You can select the <code>nullChannel</code> here to silently drop the reply messages.

<i>Required</i>


Advice can be added to change the behaviour of this endpoint, for example to add retry logic in case of failures. The following types of advice are available:

<b>Retry advice</b>: allows configuration of sophisticated retry scenarios; this includes specifying policies for retry attemps, backoff periods between attempts and the recovery strategy when retries are exhausted
<b>Circuit breaker</b>: if a certain number of consecutive attempts fails, new requests will <i>fail fast</i> and no attempt will be made to invoke the request handler again until some time has expired
<b>Expression evaluating advice</b>: general advice that evaluates a configurable <i>SpEL expression</i> on successful and/or failed attempts, and optionally can send a message to a <i>success channel</i> and/or <i>failure channel</i>

By adding multiple advices to this endpoint you can create even more complex combined behaviour. For example, if you add a <i>circuit breaker</i> and a <i>retry advice</i>, you can create a scenario where the circuit breaker only opens when all retries are exhaused. Note that the order of the advice types is important, as switching the order will change the combined behaviour: the first item in the list will be the top of the advice chain, meaning it will be the last advice that is evaluated. Also note that if any advice "traps" exceptions, all advices higher up in the chain won't know about any failures.

#### Id
Name that uniquely identifies this flow component.

<i>Required</i>

