---
title: Compatibility Matrix
description: This page presents the compatibility matrix for the Nuxeo Platform.
review:
    comment: ''
    date: '2018-07-25'
    status: ok
labels:
    - lts2016-ok
    - multiexcerpt
    - lts2017-ok
    - fguillaume
toc: true
confluence:
    ajs-parent-page-id: '3866685'
    ajs-parent-page-title: Installation
    ajs-space-key: NXDOC
    ajs-space-name: Nuxeo Platform Developer Documentation
    canonical: Compatibility+Matrix
    canonical_source: 'https://doc.nuxeo.com/display/NXDOC/Compatibility+Matrix'
    page_id: '31034423'
    shortlink: N4zZAQ
    shortlink_source: 'https://doc.nuxeo.com/x/N4zZAQ'
    source_link: /display/NXDOC/Compatibility+Matrix
tree_item_index: 200
version_override:
    LTS 2015: 710/admindoc/supported-application-servers
    '6.0': 60/admindoc/supported-application-servers
    '5.8': 58/admindoc/supported-application-servers
history:
    -
        author: Solen Guitter
        date: '2016-08-05 09:10'
        message: ''
        version: '8'
    -
        author: Solen Guitter
        date: '2016-08-05 09:08'
        message: ''
        version: '7'
    -
        author: Solen Guitter
        date: '2016-08-05 09:05'
        message: ''
        version: '6'
    -
        author: Solen Guitter
        date: '2016-08-05 09:05'
        message: Add MarkLogic
        version: '5'
    -
        author: Solen Guitter
        date: '2016-05-16 11:57'
        message: ''
        version: '4'
    -
        author: Florent Guillaume
        date: '2016-05-16 10:27'
        message: Details about Java versions supported.
        version: '3'
    -
        author: Solen Guitter
        date: '2016-05-13 15:17'
        message: ''
        version: '2'
    -
        author: Solen Guitter
        date: '2016-05-13 14:21'
        message: ''
        version: '1'
---
## Java

Supported Java versions: {{! multiexcerpt name='java_requirement'}}**JDK 11** (Oracle's JDK or OpenJDK) and greater{{! /multiexcerpt}}.

As for any software, we very strongly recommend upgrading to the latest bugfix version of the JDK for any given major version, for instance the latest bugfix version of Java 11 was 11.0.5 at the time of this writing.

More information is available from the [Installation]({{page page='installation'}}) page.

## Databases

The Nuxeo Platform supports the following databases:
{{! multiexcerpt name='all-supported-databases'}}
<ul>
<li>{{! multiexcerpt name='MariaDB-supported'}}MariaDB 10.3{{! /multiexcerpt}}</li>
<li>{{! multiexcerpt name='MongoDB-supported'}}MongoDB 4.0{{! /multiexcerpt}}</li>
<li>{{! multiexcerpt name='MySQL-supported'}}MySQL 8.0{{! /multiexcerpt}}</li>
<li>{{! multiexcerpt name='Oracle-supported'}}Oracle 18c{{! /multiexcerpt}}</li>
<li>{{! multiexcerpt name='PostgreSQL-supported'}}PostgreSQL 11{{! /multiexcerpt}}</li>
<li>{{! multiexcerpt name='SQLserver-supported'}}SQL Server 2017{{! /multiexcerpt}}</li>
</ul>
{{! /multiexcerpt}}

**Notes**

{{! multiexcerpt name='supported-databases-notes'}}
Nuxeo Platform will likely work with greater versions of the aforementioned databases. Do not hesitate to inform Nuxeo support of your attempts with different versions.
More information can be found on the [Database Configuration]({{page version='' space='nxdoc' page='database-configuration'}}) page.<br/>
Note that Nuxeo Server is shipped with an embedded H2 database, for quick evaluation purposes. One of the listed databases is required for a production set up or for a more thorough evaluation, like performance testing.
{{! /multiexcerpt}}

## Application Servers

Nuxeo Platform can be based on [Tomcat](http://tomcat.apache.org/). The supported version is:

{{! multiexcerpt name='supported-app-servers-versions'}}
<ul>
<li>Tomcat 9.0.14</li>
</ul>
{{! /multiexcerpt}}

{{! multiexcerpt name='supported-app-servers-static-war'}}
Nuxeo is shipped with an embedded Tomcat server.
{{! /multiexcerpt}}

## Redis

{{! multiexcerpt name='redis_supported_versions'}}
<div class="table-scroll">
<table class="hover">
<tbody>
<tr>
<th colspan="1">Nuxeo Platform Version:</th>
<th colspan="1">LTS 2019</th>
<th colspan="1">LTS 2017</th>
<th colspan="1">LTS 2016</th>
</tr>
<tr>
<th colspan="1">Redis</th>
<td colspan="1">2.8.x <br />
3.0.x <br />
3.2.x <br />
4.0.x</td>
<td colspan="1">2.8.x <br />
3.0.x <br />
3.2.x <br />
4.0.x</td>
<td colspan="1">2.8.x <br />
3.0.x <br />
3.2.x <br />
4.0.x</td>
</tr>
</tbody>
</table>
</div>
{{! /multiexcerpt}}

More information can be found on the [Nuxeo and Redis]({{page page='nuxeo-and-redis'}}) and [Redis Configuration]({{page page='redis-configuration'}}) pages.

## Elasticsearch

{{! multiexcerpt name='elasticsearch_supported_versions'}}
<div class="table-scroll">
<table class="hover">
<tbody>
<tr>
<th colspan="1">Nuxeo Platform Version:</th>
<th colspan="1">LTS 2019</th>
<th colspan="1">LTS 2017</th>
<th colspan="1">LTS 2016</th>
</tr>
<tr><th colspan="1">Elasticsearch</th>
<td colspan="1">
Library: 6.5.3<br/>
Cluster:
- 6.5.x to 6.8.x when using the RestClient protocol.<br/>
- 6.5.x when using the TransportClient.<br/>
</td>
<td colspan="1">
Library: 5.6.3<br/>
Cluster: 5.6.x</td>
<td colspan="1">**From 8.1 to 8.3:**<br/>
Library: 1.5.2<br/>
Cluster: 1.5.2 to 1.7.x<br/>
**From 8.10:**<br/>
Library: 2.3.5<br />
Cluster: 2.3.x to 2.4.x</td>
</tr>
</tbody>
</table>
</div>{{! /multiexcerpt}}

{{#> callout type='warning' }}
Note that there are [known problems](https://jira.nuxeo.com/browse/NXP-25252) on using the following stack:
- Elasticsearch 6.3.0
- Java 10
- Amazon latest generation instance type (c5 or m5)

For now you should either use c4 instance either c5 with java 8.
{{/callout}}

More information can be found on the [Elasticsearch Setup]({{page page='elasticsearch-setup'}}) page.

## Kafka

{{! multiexcerpt name='kafka_supported_versions'}}

<div class="table-scroll">
<table class="hover">
<tbody>
<tr>
  <th colspan="1">Nuxeo Platform Version:</th>
  <th colspan="1">LTS 2019</th>
  <th colspan="1">LTS 2017</th>
</tr>
<tr>
  <th colspan="1">Kafka</th>
<td colspan="1">
  Library: 2.1.1 scala 2.12 since HF15<br/>
  Library: 2.1.0 scala 2.12 from HF01 to HF14<br/>
  Cluster: 1.x, 2.x
</td>
<td colspan="1">
  Library: 1.0.0 scala 2.11<br/>
  Cluster: 1.x, 2.0.0
</td>
</tr>
</tbody>
</table>
</div>
{{! /multiexcerpt}}

Kafka supports backward and forward compatibility a cluster >= 1.0.0 works,
we still advice to use the latest available stable version.

## Browsers

{{! multiexcerpt name='supported-browsers'}}
Depending on the user interface addon or applications you use, the browser requirements can differ. See the relevant pages:
- [Nuxeo JSF UI]({{page version='' space='nxdoc' page='nuxeo-jsf-ui'}})
- [Nuxeo Web UI]({{page version='' space='nxdoc' page='web-ui-overview'}}#requirements)
{{! /multiexcerpt}}
