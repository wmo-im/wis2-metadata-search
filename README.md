# WMO WIS 2.0 Discovery Metadata exchange, harvesting and search pilot project

Date: 2020-05-03

Focal point: [Tom Kralidis](https://github.com/tomkralidis)

## Introduction

WIS 1.0 discovery is primarily comprised of WMO Core Metadata Profile, OAI-PMH for harvesting and SRU for search.

Current realities of the interfaces and encodings include:
- use of XML for metadata description and utilization in web applications
- based on an era of service-oriented architecture
- overloading of web architecture principles
  - using HTTP as a tunnel
  - little to no use of HTTP status codes
  - large, monolithic standards and systems
  - not "of the web" or "webby"
  - challenging for web developers to implement
  - challenging for mass market integration (search engine optimization)

As a result, WIS and weather/climate/water data services related to discovery and search should be improved to take advantage of current approaches and opportunities. 

Weather/climate/water data is by nature geospatial, and temporal.  The W3C [Spatial Data on the Web Best Practices](https://www.w3.org/TR/sdw-bp/)
provides guidelines on how to best enable spatiotemporal data to lower the barrier for users, search engine optimization and linked data.

The current evolution in data exchange standards, systems and architecture are grounded in the following:
- Resource-oriented architecture (ROA)
- Representational State Transfer (REST)
- JSON and HTML as core web formats

Following this trend is the current evolution of OGC interface standards via [OGC API](http://www.ogcapi.org), which are a clean break against legacy standards, and implement APIs using core, broad industry approaches (W3C, OpenAPI, JSON, etc.).

OGC APIs are designed to be web developer friendly and are being developed with a minimal core and extension mechanism.  Example:

- Service-oriented: ~`/api?request=GetFeature&typename=roads&featureid=5`~
- Resource-oriented: `/api/collections/roads/items/5`

### Project description
This project aims to experiment implementing WMO discovery metadata as [DCAT](https://www.w3.org/TR/vocab-dcat-2/) using the [OGC API - Records](https://github.com/opengeospatial/ogcapi-records) draft standard.  This project will also experiment actionable linkages with demonstration project 1 (AMQP/MQTT), search/access of collections of variables of NWP data, as well as enabling search capability against WIS 2.0 topics.

### WIS 2.0 Targeted Principles: 1, 2, 3, 4, 6, 10 and 11.
