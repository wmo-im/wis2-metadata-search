# WIS 2.0 Demonstration Project Charter

Date: 2020-08-26
Focal point: Tom Kralidis

## Discovery Metadata exchange, harvesting and search

### Introduction
WIS 1.0 discovery is primarily comprised of WMO Core Metadata Profile, OAI-PMH for harvesting and SRU for search.

Current realities of the interfaces and encodings include:
-	use of XML for metadata description and utilization in web applications
- based on an era of service-oriented architecture
- overloading of web architecture principles
  - using HTTP as a tunnel
  - little to no use of HTTP status codes
  - large, monolithic standards and systems
  - not "of the web" or "webby"
  - challenging for web developers to implement
  - challenging for mass market integration (search engine optimization)

As a result, WIS and weather/climate/water data and services related to discovery and search should be improved to take advantage of current approaches and opportunities. 

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

### Project objectives
This project aims to experiment implementing WMO discovery metadata as [DCAT](https://www.w3.org/TR/vocab-dcat-2/) using the [OGC API - Records](https://github.com/opengeospatial/ogcapi-records) draft standard.  This project will also experiment actionable linkages with demonstration project 1 (AMQP/MQTT), search/access of collections of variables of NWP data, as well as enabling search capability against WIS 2.0 topics.

### WIS 2.0 Principles demonstrated

This project will demonstrate the following WIS 2.0 principles.

- 1 *WIS 2.0: adopts Web technologies and leverages industry best practices and open standards*: the project will implement HTTP, RESTful design patterns, as well as the evolving OGC API suite of standards

- 2 *WIS 2.0: uses Uniform Resource Locators (URL) to identify resources (i.e. Web pages, data, metadata, APIs)*: the project will implement link relations in support of the hypermedia

- 3 *WIS 2.0: prioritizes use of public telecommunications networks (i.e. the Internet) when publishing digital resources*: the project will use the Web as the platform

- 4 *WIS 2.0: requires provision of Web service(s) to access or interact with digital resources (e.g. data, information, products) published using WIS*: the project will implement discovery as a web service (API) as well as hypermedia controls to related actionable bindable services/APIs

- 6 *WIS 2.0: will add open standard messaging protocols that use the publish-subscribe message pattern to the list of data exchange mechanisms approved for use within WIS and GTS*: this project will demonstrate actionable hypermedia controls to protocols and services put forth in Demonstration project 1 (Exploring the use of message querying protocols for GTS data exchange)

- 10 *WIS 2.0: will provide a catalogue containing metadata that describes both data and the service(s) provided to access that data*: this project will demonstrate OGC API - Records as an approach for cataloguing WIS metadata for data and services

- 11 *WIS 2.0: encourages data providers to publish metadata describing their data and Web services in a way that can be indexed by commercial search engines*: this project will enable WIS metadata for SEO and mass market interoperability

### Deliverables
- open source client and server implementation of OGC API - Records standard
- demonstration of harvesting, discovery and search capability between search client/server implementations
- report of the demonstration (design, implementation, future work, recommendations)

### Milestones

|Milestone|Date|
|---|-----|
|metadata design (types, crosswalk)|2021-03-31|
|demonstration (harvesting, search)|2021-09-30|
|final report|2021-10-31|
