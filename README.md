# Docker MySQL Java Container

[![Build Status](https://travis-ci.org/UKHomeOffice/docker-mysql-java.svg?branch=master)](https://travis-ci.org/UKHomeOffice/docker-mysql-java)

Docker MySQL Container that also includes Open Java 8 *JRE* install.

## Getting Started

These instructions will cover usage information and for the docker container 

### Prerequisities

In order to run this container you'll need docker installed.

* [Windows](https://docs.docker.com/windows/started)
* [OS X](https://docs.docker.com/mac/started/)
* [Linux](https://docs.docker.com/linux/started/)

### Usage

This is intended as a base image that would extended mysql so Java code maybe run along with mysql tools installed e.g.


```
FROM quay.io/ukhomeofficedigital/mysql-java:v0.1.2

# Customisations to allow for schema updates using liquidbase Java file
# =====================================================================

ENV TERM dumb

COPY docker-entrypoint.sh /

ENTRYPOINT ["/docker-entrypoint.sh"]
```

It was created to run a simple bash mysql users script and then run a Java 
[Liquidbase](http://www.liquibase.org/) schema install.

It extends the mysql only repository and as such, most of the documentation is available here:
[Docker MySQL](https://github.com/UKHomeOffice/docker-mysql/blob/v0.5.1/README.md)

 

## Contributing

Feel free to submit pull requests and issues. If it's a particualy large PR, you may wish to discuss
it in an issue first.

Please note that this project is released with a [Contributor Code of Conduct](code_of_conduct.md). 
By participating in this project you agree to abide by its terms.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the 
[tags on this repository](https://github.com/UKHomeOffice/docker-mysql-java/tags). 

## Authors

* **Lewis Marshall** - *Initial work* - [Lewis Marshall](https://github.com/LewisMarshall)

See also the list of [contributors](https://github.com/UKHomeOffice/docker-mysql-java/contributors) who 
participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

* This container is taken from the 
  [UKHomeOffice mysql docker container](https://quay.io/repository/ukhomeofficedigital/mysql).
