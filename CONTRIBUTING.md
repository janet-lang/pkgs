# Guidelines for contributing to the Janet Package Listing

Thanks for taking time to contribute!

Please read this document before making contributions.

## Adding a Package

* Check if the package exists before adding it twice.
* The name of the package should usually be the same as that of its
  git repository, and should be all lower case and in kebab-case.
  For example, use `my-package` as a package name, not `mypackage` or `MyPackage`.
* Make sure that your package can be used with `jpm`. This means it
  should have a file `project.janet` in it's root directory, and should run properly when installed via `jpm install https://some.git-host.org/me/mypackage.git`. Do not add packages that do not work with jpm! If jpm cannot support your package, open an issue in the [Janet](https://github.com/janet-lang/janet) repository and we will see what we can do.

### Good package names

* `my-package`
* `thing`
* `thing@bakpakin` (for a fork of the package)

### Bad package names

* `mypackage`
* `my_package`
* `MyPackage`
* `my package`
* `my.package.git`
* `org.this.is.not.java.AbstractWidgetFactoryProducer`

If you would like to add a package here, just open a pull request with the name and URL of the package and edit the pkgs.janet file.

## Broken Links

Please open issues if you find broken links. Try also to find the correct link or at least
the reason a link is broken. We can then update or remove offending packages.
