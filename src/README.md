# Groovy access to QADB

This directory contains the Groovy source code to access the QA database

- first, set environment variables with `source ../environ.sh`
- then run your analysis script with `run-groovy`, a groovy wrapper script
  provided by `coatjava` (at `$COATJAVA/bin/run-groovy`)
- see example scripts in `examples/` directory
  - a standard usage of QA cuts is demonstrated in
    [`examples/cutCustom.groovy`](examples/cutCustom.groovy)
- usage notes:
  - include the `QADB` class with `import clasqa.QADB`, then instantiate
  - the `QADB` class provides several methods for accessing the QA info;
    you only need to provide it a run number and event number
  - database lookups are only performed as needed, so it is safe to
    use any accessor method in a standard analysis event loop
