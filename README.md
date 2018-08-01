[Quasi](http://github.com/fromage/quasi) is a Java library that
provides high-performance lightweight threads, via a fork of the Quasar
library. Quasi fibers rely on bytecode
instrumentation. This can be done at classloading time via a Java Agent, or at
compilation time. This project ships a Maven plugin for the ahead-of-time Quasi
instrumentation of the compiled class files.

Usage
=====

Configure the plugin to instrument the code:

    <plugin>
        <groupId>com.github.fromage.quasi</groupId>
        <artifactId>quasi-maven-plugin</artifactId>
        <version>0.7.5</version>
        <configuration>
            <check>true</check>
            <debug>true</debug>
            <verbose>true</verbose>
        </configuration>
        <executions>
            <execution>
                <goals>
                    <goal>instrument</goal>
                </goals>
            </execution>
        </executions>
    </plugin>

License
=======

This project is licensed under
[The BSD 3-Clause License](http://opensource.org/licenses/BSD-3-Clause).
