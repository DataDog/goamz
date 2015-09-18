# goamz - An Amazon Library for Go

[![Build Status](http://travis-ci.org/goamz/goamz.png?branch=master)](https://travis-ci.org/goamz/goamz)

The _goamz_ package enables Go programs to interact with Amazon Web Services.

This is a fork of the version [developed within Canonical](https://wiki.ubuntu.com/goamz) with additional functionality and services from [a number of contributors](https://github.com/DataDog/goamz/contributors)!

The API of AWS is very comprehensive, though, and goamz doesn't even scratch the surface of it. That said, it's fairly well tested, and is the foundation in which further calls can easily be integrated. We'll continue extending the API as necessary - Pull Requests are _very_ welcome!

The following packages are available at the moment:

```
github.com/DataDog/goamz/autoscaling
github.com/DataDog/goamz/aws
github.com/DataDog/goamz/cloudformation
github.com/DataDog/goamz/cloudfront
github.com/DataDog/goamz/cloudwatch
github.com/DataDog/goamz/dynamodb
github.com/DataDog/goamz/ecs
github.com/DataDog/goamz/ec2
github.com/DataDog/goamz/elb
github.com/DataDog/goamz/iam
github.com/DataDog/goamz/rds
github.com/DataDog/goamz/route53
github.com/DataDog/goamz/s3
github.com/DataDog/goamz/sqs
github.com/DataDog/goamz/sts

github.com/DataDog/goamz/exp/mturk
github.com/DataDog/goamz/exp/sdb
github.com/DataDog/goamz/exp/sns
```

Packages under `exp/` are still in an experimental or unfinished/unpolished state.

## API documentation

The API documentation is currently available at:

[http://godoc.org/github.com/DataDog/goamz](http://godoc.org/github.com/DataDog/goamz)

## How to build and install goamz

Just use `go get` with any of the available packages. For example:

* `$ go get github.com/DataDog/goamz/ec2`
* `$ go get github.com/DataDog/goamz/s3`

## Running tests

To run tests, first install gocheck with:

`$ go get gopkg.in/check.v1`

Then run go test as usual:

`$ go test github.com/DataDog/goamz/...`

_Note:_ running all tests with the command `go test ./...` will currently fail as tests do not tear down their HTTP listeners.

If you want to run integration tests (costs money), set up the EC2 environment variables as usual, and run:

$ gotest -i
