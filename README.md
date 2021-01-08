# pkgs

The official package listing for Janet. It maps short package
names to full git urls for use in scripts and Janet programs.

If you have written a Janet library that you think others may
find useful, please submit a pull-request here adding it to
the package listing. Thanks!


## Usage (from jpm)

For convenience, packages listed here may be installed using
just their short name, for example:

    [sudo] jpm install path
    # rather than
    [sudo] jpm install https://github.com/janet-lang/path.git


## Usage (from Janet)

```clojure
(import pkgs)

(pp pkgs/packages)
```
