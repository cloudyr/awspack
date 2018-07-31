# Amazon Web Services Bundle Package

**awspack** is a bundle of all of [the cloudyr project's](http://cloudyr.github.io) packages for Amazon Web Services (AWS). It depends upon all of the cloudyr project's AWS packages. It is mainly useful for installing the entire suite of packages; more likely than not you will only want to load individual packages one at a time.

To use the package, you will need an AWS account and to enter your credentials into R. Your keypair can be generated on the [IAM Management Console](https://aws.amazon.com/) under the heading *Access Keys*. Note that you only have access to your secret key once. After it is generated, you need to save it in a secure location. New keypairs can be generated at any time if yours has been lost, stolen, or forgotten. The [**aws.iam** package](https://github.com/cloudyr/aws.iam) profiles tools for working with IAM, including creating roles, users, groups, and credentials programmatically; it is not needed to *use* IAM credentials.

A detailed description of how credentials can be specified is provided at: https://github.com/cloudyr/aws.signature/. The easiest way is to simply set environment variables on the command line prior to starting R or via an `Renviron.site` or `.Renviron` file, which are used to set environment variables in R during startup (see `? Startup`). They can be also set within R:

```R
Sys.setenv("AWS_ACCESS_KEY_ID" = "mykey",
           "AWS_SECRET_ACCESS_KEY" = "mysecretkey",
           "AWS_DEFAULT_REGION" = "us-east-1",
           "AWS_SESSION_TOKEN" = "mytoken")
```

## Installation

[![CRAN](https://www.r-pkg.org/badges/version/awspack)](https://cran.r-project.org/package=awspack)
![Downloads](https://cranlogs.r-pkg.org/badges/awspack)
[![Travis Build Status](https://travis-ci.org/cloudyr/awspack.png?branch=master)](https://travis-ci.org/cloudyr/awspack)
[![codecov.io](https://codecov.io/github/cloudyr/awspack/coverage.svg?branch=master)](https://codecov.io/github/cloudyr/awspack?branch=master)

To install the latest development version you can install from the cloudyr drat repository:

```R
# latest stable version
install.packages("awspack", repos = c(cloudyr = "http://cloudyr.github.io/drat", getOption("repos")))
```

Or, to pull a potentially unstable version directly from GitHub:

```R
if (!require("remotes")) {
    install.packages("remotes")
}
remotes::install_github("cloudyr/awspack")
```

---
[![cloudyr project logo](http://i.imgur.com/JHS98Y7.png)](https://github.com/cloudyr)
