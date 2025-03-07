# httr

<!-- badges: start -->
[![CRAN status](https://www.r-pkg.org/badges/version/httr)](https://cran.r-project.org/package=httr)
[![R-CMD-check](https://github.com/r-lib/httr/workflows/R-CMD-check/badge.svg)](https://github.com/r-lib/httr/actions)
[![Codecov test coverage](https://codecov.io/gh/r-lib/httr/branch/master/graph/badge.svg)](https://app.codecov.io/gh/r-lib/httr?branch=main)
<!-- badges: end -->

The aim of httr is to provide a wrapper for the [curl](https://cran.r-project.org/package=curl) package, customised to the demands of modern web APIs.

Key features:

* Functions for the most important http verbs: `GET()`, `HEAD()`, `PATCH()`, 
  `PUT()`, `DELETE()` and `POST()`.

* Automatic connection sharing across requests to the same website (by
  default, curl handles are managed automatically), cookies are maintained
  across requests, and a up-to-date root-level SSL certificate store is used.

* Requests return a standard reponse object that captures the http status line,
  headers and body, along with other useful information.

  * Response content is available with `content()` as a raw vector (`as =
    "raw"`), a character vector (`as = "text"`), or parsed into an R object
    (`as = "parsed"`), currently for html, xml, json, png and jpeg.

  * You can convert http errors into R errors with `stop_for_status()`.

* Config functions make it easier to modify the request in common ways:
  `set_cookies()`, `add_headers()`, `authenticate()`, `use_proxy()`, 
  `verbose()`, `timeout()`, `content_type()`, `accept()`, `progress()`.

* Support for OAuth 1.0 and 2.0 with `oauth1.0_token()` and `oauth2.0_token()`.
  The demo directory has eight OAuth demos: four for 1.0 (twitter, vimeo,
  withings and yahoo) and four for 2.0 (facebook, github, google, linkedin). 
  OAuth credentials are automatically cached within a project. 

httr wouldn't be possible without the hard work of the authors of [curl](https://cran.r-project.org/package=curl) and [libcurl](https://curl.se/). Thanks! httr is inspired by http libraries in other languages, such as [Resty](http://beders.github.io/Resty/Resty/Examples.html), [Requests](https://requests.readthedocs.io/en/master/) and [httparty](https://github.com/jnunemaker/httparty/tree/master).

## Installation

To get the current released version from CRAN:

```R
install.packages("httr")
```

To get the current development version from github:

```R
# install.packages("devtools")
devtools::install_github("r-lib/httr")
```

## Code of Conduct

Please note that the httr project is released with a [Contributor Code of Conduct](https://httr.r-lib.org/CODE_OF_CONDUCT.html). By contributing to this project, you agree to abide by its terms.
