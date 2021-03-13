---
layout: page
title: My projects
---

# Tjahzi

[![License: MIT](https://img.shields.io/github/license/tkowalcz/tjahzi?style=for-the-badge)](https://github.com/tkowalcz/tjahzi/blob/master/LICENSE)
[![CircleCI](https://img.shields.io/circleci/build/github/tkowalcz/tjahzi?style=for-the-badge)](https://app.circleci.com/pipelines/github/tkowalcz/tjahzi?branch=master)
[![Maven Central](https://img.shields.io/maven-central/v/pl.tkowalcz.tjahzi/core.svg?label=Core&style=for-the-badge)](https://search.maven.org/search?q=g:pl.tkowalcz.tjahzi)

[![Maven Central](https://img.shields.io/maven-central/v/pl.tkowalcz.tjahzi/log4j2-appender.svg?label=Log4j2%20Appender&style=for-the-badge)](https://search.maven.org/search?q=g:pl.tkowalcz.tjahzi)
[![Maven Central](https://img.shields.io/maven-central/v/pl.tkowalcz.tjahzi/logback-appender.svg?label=Logback%20Appender&style=for-the-badge)](https://search.maven.org/search?q=g:pl.tkowalcz.tjahzi)

It is a Java client for Grafana Loki. It has a core component that implements sending batches of logs to Loki. On top of it
we built log4j2 and Logback appenders, with following main advantages: 

1. Logging does not allocate objects nor take any locks.
1. Sending data to Loki in batches allocates as little as possible.
1. We also provide a no-dependency version of log4j2 appender.
1. Includes in-house implementation of protobuf wire format for Loki to reduce dependencies and improve performance

Tjahzi is currently used to ship logs from tens of servers at about 10GB of logs per day.

#### Log4j2

Dependency info:
```xml
<dependency>
    <groupId>pl.tkowalcz.tjahzi</groupId>
    <artifactId>log4j2-appender-nodep</artifactId>
    <version>0.9.5</version>
</dependency>
```

For `log4j2` appender quick start guide and detailed discussions see this [README.md](https://github.com/tkowalcz/tjahzi/blob/master/log4j2-appender/README.md).

#### Logback

Dependency info:
```xml
<dependency>
  <groupId>pl.tkowalcz.tjahzi</groupId>
  <artifactId>logback-appender-nodep</artifactId>
  <version>0.1.0</version>
</dependency>
```

For `Logback` appender quick start guide and detailed discussions see this [README.md](https://github.com/tkowalcz/tjahzi/blob/master/logback-appender/README.md).
