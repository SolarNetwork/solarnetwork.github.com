---
layout: post
title: OSCP Flexibility Provider
tags: oscp, ocpp, solarnet
category: news
---
SolarNetwork has added an [Open Smart Charging Protocol][oscp] 2.0 [Flexibility Provider
service][solarnet-oscp], to support demand-response forecast signals from electric grid operators.
The OSCP Flexibility Provider service allows grid operators to send detailed grid constraint
forecasts to SolarNetwork. These forecasts contain information like:

> between 13:00 - 13:15 use no more than 50 kW of total power at grid connection point ABC

The forecasts are
turned into datum streams that can be handled through standard SolarNetwork integration methods like
[SolarFlux][solarflux] and [SolarQuery][solarquery]. Distributed energy resources can then be
managed appropriately via [instructions][instr], such as limiting the charge rates of EV chargers
integrated with SolarNetwork via [OCPP][solarnet-ocpp].

<img src="{{site.baseurl}}/images/news/evisi-logo-195.png" alt="EVisi" width="98" style="float: left; margin-right: 1em;"/>
This feature was developed with support from our friends at [EVisi](https://evisi.co/).

[instr]: https://github.com/SolarNetwork/solarnetwork/wiki/SolarUser-API#queue-instruction
[oscp]: https://www.openchargealliance.org/protocols/oscp-20/
[solarflux]: https://github.com/SolarNetwork/solarnetwork/wiki/SolarFlux-API
[solarnet-ocpp]: https://github.com/SolarNetwork/solarnetwork/wiki/OCPP
[solarnet-oscp]: https://github.com/SolarNetwork/solarnetwork/wiki/OSCP
[solarquery]: https://github.com/SolarNetwork/solarnetwork/wiki/SolarQuery-API
[solaruser-oscp-api]: https://github.com/SolarNetwork/solarnetwork/wiki/SolarUser-OSCP-API
