---
layout: post
title: SolarNetwork data expire feature added
tags: dev, data
---
SolarNetwork has a new feature that allows configuring data retention policies so data collected by
the SolarNodes in your account can be automatically purged after it is no longer useful.

One especially nice aspect of this feature is that the rolled-up hourly, daily, and monthly
aggregate data SolarNetwork automatically computes can be retained if desired, only deleting the
fine-grained "raw" collected data. For accounts on paid subscriptions, this provides an easy way to
keep your long-term storage costs down while retaining a full history of your data.

![expire-ui]({{site.baseurl}}/images/news/solaruser-data-expire-ui.png)

The expiration policy page even allows you to "preview" what would happen if the policy were
activated, by showing you a tally of the data that would be deleted:

![expire-preview]({{site.baseurl}}/images/news/solaruser-expire-policy-preview.png)
