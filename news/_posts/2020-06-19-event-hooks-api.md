---
layout: post
title: Node event hooks API added
tags: dev, solaruser
---
SolarUser has a new set of REST endpoints under
[/user/event/node](https://github.com/SolarNetwork/solarnetwork/wiki/SolarUser-Event-Hook-API#endpoints)
that are designed to support configuring "hooks" into external applications based on node-related
events happening in SolarNetwork. This feature is essentially "push notifications" for SolarNetwork.

![SolarUser node event hook UI]({{site.baseurl}}/images/news/solaruser-node-event-hook-ui.png)

## Events

To start there is one event that can be hooked into: aggregate processing. When SolarNetwork computes
an aggregate datum an event is generated that you can configure a hook for. This can be useful 
when you have an application that wants to derive some data out of the aggregate data in SolarNetwork
and keep it synchronized and up-to-date with what's in SolarNetwork.

For example, you might have an application that calculates the hourly cost associated with an energy
datum source. Using this new hook API, your application can be called each time SolarNetwork
computes the hourly energy value for that source. Your application could even store its result 
back in SolarNetwork, making a new datum source derived out of the original one!

## Services

To start there is one supported hook service: publishing the event to 
[AWS Simple Queue Service (SQS)][sqs]. See the [SQS service documentation][sqs-service] for details
on how it can be configured.


<img src="{{site.baseurl}}/images/news/ecogy-logo-248.png" alt="Ecogy Energy" width="62" style="float: left; margin-right: 1em;"/>
This feature was developed with support from our friends at [Ecogy Energy](https://www.ecogysolar.com/).

[sqs]: https://aws.amazon.com/sqs/
[sqs-service]: https://github.com/SolarNetwork/solarnetwork/wiki/SolarUser-Event-Hook-API#sqs-hook-service