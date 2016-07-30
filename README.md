# lein-nvd
[![Build Status](https://travis-ci.org/rm-hull/lein-nvd.svg?branch=master)](http://travis-ci.org/rm-hull/lein-nvd) [![Coverage Status](https://coveralls.io/repos/rm-hull/lein-nvd/badge.svg?branch=master)](https://coveralls.io/r/rm-hull/lein-nvd?branch=master) [![Dependencies Status](https://jarkeeper.com/rm-hull/lein-nvd/status.svg)](https://jarkeeper.com/rm-hull/lein-nvd) [![Downloads](https://jarkeeper.com/rm-hull/lein-nvd/downloads.svg)](https://jarkeeper.com/rm-hull/lein-nvd) [![Clojars Project](https://img.shields.io/clojars/v/lein-nvd.svg)](https://clojars.org/lein-nvd)

> NOT FIT FOR HUMAN CONSUMPTION JUST YET...

[National Vulnerability Database](https://nvd.nist.gov/) dependency-checker plugin for Leiningen.

### Installation

Put `[lein-nvd "0.1.0"]` into the `:plugins` vector of your `:user` profile.

## Usage

Run `lein nvd check` in your project. The first time the plugin runs, it
will download (and cache) various databases from https://nvd.nist.gov and
periodically check and update them on subsequent runs. A suite of reports
will be produced in the project's **target/nvd** directory.

### Example

There is an [example project](https://github.com/rm-hull/lein-nvd/blob/master/example/project.clj)
which has dependencies with known vulnerabilities ([CVE-2016-3720](https://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2016-3720)).
This can be demonstrated by running the following:

    $ cd example
    $ lein nvd check

This will create dependency-check reports (both HTML & XML) in **example/target/nvd**
as follows:

![report](https://raw.githubusercontent.com/rm-hull/lein-nvd/master/example/report.png)

## References

* https://nvd.nist.gov/
* https://github.com/jeremylong/DependencyCheck

## License

The MIT License (MIT)

Copyright (c) 2016 Richard Hull

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
