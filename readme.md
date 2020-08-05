# JQAssistant Maven Analyzer

Maven project for analyzing with JQAssistant.

Can be used by itself, as a gateway to use JQAssistant. Or may be used as a basis to set up JQAssistant on a Maven project.

[![Release docs](https://img.shields.io/badge/docs-release-blue.svg)][site-release]
[![Development docs](https://img.shields.io/badge/docs-develop-blue.svg)][site-develop]

[![Release javadocs](https://img.shields.io/badge/javadocs-release-blue.svg)][javadoc-release]
[![Development javadocs](https://img.shields.io/badge/javadocs-develop-blue.svg)][javadoc-develop]

## Features

The project by default comes with a useful series of features:

- Preconfigured POM to begin developing a new library fast.
- Prepared for [Travis CI](https://travis-ci.org/), including configuration files and deployment scripts. Check the [Archetype documentation](http://docs.bernardomg.com/maven/library-maven-archetype) to find out more.
- Unit and integration tests suites ready to be run with [JUnit](http://junit.org) just by using the Maven test and verify commands.
- A Maven site, using the [Docs Maven Skin](https://github.com/Bernardo-MG/docs-maven-skin), to contain the documentation, the Javadocs and several reports.
- A bunch of useful files, such as readme, gitignore and gitattributes.

## Documentation

Documentation is always generated for the latest release, kept in the 'master' branch:

- The [latest release documentation page][site-release].
- The [latest release Javadoc site][javadoc-release].

Documentation is also generated from the latest snapshot, taken from the 'develop' branch:

- The [the latest snapshot documentation page][site-develop].
- The [latest snapshot Javadoc site][javadoc-develop].

### Building the docs

The documentation site is actually a Maven site, and its sources are included in the project. If required it can be generated by using the following Maven command:

```
$ mvn verify site
```

The verify phase is required, otherwise some of the reports won't be generated.

## Usage

The application is coded in Java, using Maven to manage the project.

It is a Java library, meant to be included as a dependency on any project which may want to make use of it.

### Prerequisites

JDK 8 or higher is required. All other dependencies are handled through Maven, and noted in the included POM file.

### Installing

The recommended way to install the project is by setting it up as a dependency. To get the configuration information for this check the [Bintray repository][bintray-repo], or the [Maven Central Repository][maven-repo].

It is always possible installing it by using the usual Maven command:

```
$ mvn install
```

## Collaborate

Any kind of help with the project will be well received, and there are two main ways to give such help:

- Reporting errors and asking for extensions through the issues management
- or forking the repository and extending the project

### Issues management

Issues are managed at the GitHub [project issues tracker][issues], where any Github user may report bugs or ask for new features.

### Getting the code

If you wish to fork or modify the code, visit the [GitHub project page][scm], where the latest versions are always kept. Check the 'master' branch for the latest release, and the 'develop' for the current, and stable, development version.

## License

The project has been released under the [MIT License][license].

[bintray-repo]: https://bintray.com/bernardo-mg/maven/jqassistant-maven-analyzer/view
[maven-repo]: http://mvnrepository.com/artifact/com.bernardomg.jqassistant/jqassistant-maven-analyzer
[issues]: https://github.com/bernardo-mg/jqassistant-maven-analyzer/issues
[javadoc-develop]: https:///jqassistant-maven-analyzer/apidocs
[javadoc-release]: https:///jqassistant-maven-analyzer/apidocs
[license]: https://www.opensource.org/licenses/mit-license.php
[scm]: https://github.com/bernardo-mg/jqassistant-maven-analyzer
[site-develop]: https:///jqassistant-maven-analyzer
[site-release]: https:///jqassistant-maven-analyzer
