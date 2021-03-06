Metrics Plugin for Graylog
==========================

[![Github Downloads](https://img.shields.io/github/downloads/graylog-labs/graylog-plugin-metrics/total.svg)](https://github.com/graylog-labs/graylog-plugin-metrics/releases)
[![GitHub Release](https://img.shields.io/github/release/graylog-labs/graylog-plugin-metrics.svg)](https://github.com/graylog-labs/graylog-plugin-metrics/releases)
[![Build Status](https://travis-ci.org/graylog-labs/graylog-plugin-metrics.svg)](https://travis-ci.org/graylog-labs/graylog-plugin-metrics)

An output plugin for integrating [Graphite](http://graphite.readthedocs.org), [Ganglia](http://ganglia.info) and [StatsD](https://github.com/etsy/statsd) with [Graylog](https://www.graylog.org).

**Required Graylog version:** 2.0 and later

Please use version 1.2.0 of this plugin if you run Graylog 1.x

## Installation

[Download the plugin](https://github.com/graylog-labs/graylog-plugin-metrics/releases)
and place the `.jar` file in your Graylog plugin directory. The plugin directory
is the `plugins/` folder relative from your `graylog-server` directory by default
and can be configured in your `graylog.conf` file.

Restart `graylog-server` and you are done.

## Build

This project is using Maven and requires Java 8 or higher.

You can build a plugin (JAR) with `mvn package`.

DEB and RPM packages can be build with `mvn jdeb:jdeb` and `mvn rpm:rpm` respectively.

## Plugin Release

We are using the maven release plugin:

```
$ mvn release:prepare
[...]
$ mvn release:perform
```

This sets the version numbers, creates a tag and pushes to GitHub. TravisCI will build the release artifacts and upload to GitHub automatically.
