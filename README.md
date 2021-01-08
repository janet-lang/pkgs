# pkgs

The official package listing for Janet. It maps short package
names to full git urls for use in scripts and Janet programs.

To have your own library added to the package listing, please see
the CONTRIBUTING document. Thanks!


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
