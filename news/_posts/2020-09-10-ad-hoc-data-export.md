---
layout: post
title: Ad hoc data export UI in SolarUser
tags: dev, solaruser
---
SolarUser has a supported scheduled data exports [for a couple of years now]({% post_url
/news/2018-05-01-data-export %}), and the SolarUser API has supported [ad hoc data
exports][ad-hoc-export-submit] for more than a year. Now we've added an easy-to-use UI in the
[SolarUser Data Export][solaruser-data-export] page for submitting ad hoc data exports. Just fill in
a simple form to pick the date range, nodes, sources, and aggregate level you want to export:

![SolarUser ad hoc export form]({{site.baseurl}}/images/news/solaruser-adhoc-datum-export-create.png)

Once submitted, the export jobs show up with status information:

![SolarUser ad hoc exports]({{site.baseurl}}/images/news/solaruser-adhoc-datum-exports.png)

<img src="{{site.baseurl}}/images/news/ecogy-logo-248.png" alt="Ecogy Energy" width="62" style="float: left; margin-right: 1em;"/>
This feature was developed with support from our friends at [Ecogy Energy](https://ecogyenergy.com/).

[solaruser-data-export]: https://data.solarnetwork.net/solaruser/u/sec/export
[ad-hoc-export-submit]: https://github.com/SolarNetwork/solarnetwork/wiki/SolarUser-Datum-Export-API#submit-ad-hoc-export-task