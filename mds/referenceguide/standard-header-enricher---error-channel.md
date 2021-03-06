---
id: standard-header-enricher---error-channel
title: Standard header enricher - Error channel
sidebar_label: Standard header enricher - Error channel
---
#### Channel reference
Specifies the channel which id is used as value for the header.

#### Expression
SpEL (Spring Expression Language) expression that computes the value. Result must be the id of a channel.

Example:
<code>headers.foo + '-channel'</code>

See also: 
<a href="http://static.springsource.org/spring/docs/3.0.x/reference/expressions.html" target="_blank>SpEL documentation</a>

#### Overwrite
Boolean value to indicate whether this header value should overwrite an existing header value for the same name.

Default is 'false'.

