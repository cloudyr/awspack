# Amazon Web Services Bundle Package

**awspack** is a bundle of all of [the cloudyr project's](http://cloudyr.github.io) packages for Amazon Web Services (AWS). It depends upon all of the cloudyr project's AWS packages. It is mainly useful for installing the entire suite of packages; more likely than not you will only want to load individual packages one at a time.

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
if (!require("ghit")) {
    install.packages("ghit")
}
ghit::install_github("cloudyr/awspack")
```

---
[![cloudyr project logo](http://i.imgur.com/JHS98Y7.png)](https://github.com/cloudyr)
