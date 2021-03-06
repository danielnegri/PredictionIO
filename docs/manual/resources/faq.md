---
layout: docs
title: FAQ
---

# Frequently Asked Questions

|

### Question: How to resolve "Error: Could not find or load main class io.prediction.tools.Console" after ./make_distribution.sh?

```
$ bin/pio app
Error: Could not find or load main class io.prediction.tools.Console
```

When PredictionIO bumps a version, it creates another JAR file with the new
version number.

Delete everything but the latest `pio-assembly-<VERSION>.jar` in
`$PIO_HOME/assembly` directory. For example:

```
PredictionIO$ cd assembly/
PredictionIO/assembly$ ls -al
total 197776
drwxr-xr-x  2 yipjustin yipjustin      4096 Nov 12 00:08 .
drwxr-xr-x 17 yipjustin yipjustin      4096 Nov 12 00:09 ..
-rw-r--r--  1 yipjustin yipjustin 101184982 Nov  5 06:05 pio-assembly-0.8.1-SNAPSHOT.jar
-rw-r--r--  1 yipjustin yipjustin 101324859 Nov 12 00:09 pio-assembly-0.8.2.jar

PredictionIO/assembly$ rm pio-assembly-0.8.1-SNAPSHOT.jar
```

|

### Question: How do I increase the JVM heap size of the Event Server?

```
$ JAVA_OPTS=-Xmx16g bin/pio eventserver --ip 0.0.0.0 --port 7071
````

If you have other questions, you can search or post on the [user
group](https://groups.google.com/forum/#!forum/predictionio-user) or [email the
core team](mailto:support@prediction.io) directly.
