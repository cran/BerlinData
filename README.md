[![Build Status](https://travis-ci.org/dirkschumacher/RBerlinData.svg?branch=master)](https://travis-ci.org/dirkschumacher/RBerlinData)
BerlinData
===========

The `R` package `BerlinData` gives you easy access to [data.berlin.de](http://daten.berlin.de). This is currently the development version.

Also check out the [project website](http://dirkschumacher.github.io/RBerlinData).

# Installation

To get the current released version from CRAN (not yet available):

```R
install.packages("BerlinData")
```

To get the current development version from github:

```R
# install.packages("devtools")
devtools::install_github("dirkschumacher/RBerlinData")
```


# Usage
```R
result <- searchBerlinDatasets(query = "stolpersteine")
summary(result)
dataset <- getDatasetMetaData(result[[2]])
summary(dataset)
resource_list <- resources(dataset)
summary(resource_list)
data <- download(resource_list[[1]])
```

# Versioning
It uses [Semantic Versioning 2](http://semver.org/spec/v2.0.0.html) for version numbering.
