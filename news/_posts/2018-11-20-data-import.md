---
layout: post
title: SolarNetwork data import feature added
tags: dev, data
---
SolarNetwork has a new feature designed to help you migrate data collected from other systems into
SolarNetwork. The new **Data Import** page allows you to upload a CSV file with the data you want to
import:

![import-job-form]({{site.baseurl}}/images/news/solaruser-import-job-form.png)

Once the data is uploaded, you can preview how SolarNetwork will interpret the data, and verify
everything looks correct:

![import-job-form]({{site.baseurl}}/images/news/solaruser-import-job-preview.png)

When you finally confirm that the data should be imported, SolarNetwork will schedule the
data to be imported, and provide feedback during the import process:

![import-job-form]({{site.baseurl}}/images/news/solaruser-import-job-feedback.png)

When the import completes, SolarNetwork will show you how many datum were imported:

![export-ui]({{site.baseurl}}/images/news/solaruser-import-job-success.png)

In the future we hope to expand the number of data formats SolarNetwork can accept, and make it as
easy as possible to import data from a variety of common monitoring systems.

<img src="{{site.baseurl}}/images/news/ecogy-logo-248.png" alt="Ecogy Energy" width="62" style="float: left; margin-right: 1em;"/>
This feature was developed with support from our friends at [Ecogy Energy](https://www.ecogysolar.com/).
