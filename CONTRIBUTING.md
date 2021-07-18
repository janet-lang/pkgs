# Guidelines for contributing to the Janet package listing

Thanks for taking the time to contribute!

Please read this document before making contributions. If you find anything
missing of not appropriate, please do not hesitate and create an issue in this
repository.

## Adding a package

If you would like to add a package here, open a pull request with the package's
name and URL, and edit the `pkgs.janet` file. Bonus points for including a simple
description in your comment, and reasons why you are adding the package. Be sure
to check if the package is already listed here (packages are listed alphabetically).

Your pull request is more likely to be merged if your package meets these requirements:

* Make sure that users can use your package with `jpm`. It must have a
  `project.janet` file in its root directory, and run properly when installed via
  `jpm install https://git-host.example.org/path/to/your/package.git`. Only add
  a package that works with `jpm`! If `jpm` cannot support your package,
  open an issue in this repository, and we will see what we can do.
* Your `project.janet` file should have fields:
  * `:name`, the desired name of the package. The package's name should
    usually be the same as its git repository name. 
    Common exceptions include having a `janet-` prefix in the git repo name, but not in the package name.
    One exception is the `janet-` prefix in the git repository name to
    avoid name clashes. The name should also avoid clashing with existing names in pkgs.
  * `:author`, name of the author of the package. Preferably with email contact
    in the standard format: `"Josef Pospíšil <josef.pospisil@laststar.eu>"`.
  * `:description`, short informative description of the package, preferably one
    sentence.
  * `:license`, abbreviation of the license name, e.g., "MIT".
  * `:url`, further information about the package. It could be a link to the
    project's repository, home page with `README.md`, or any other website.
  * `:repo`, from which users could clone its source code.
  * `:dependencies`, if this package depends on other packages. 
     Ideally, all of the dependencies will already exist in the pkgs list.
* Add package license, preferably in a `LICENSE` file in the root of the
  project.


## Optional package properties

These are not required (at least for now) but are nice to have for any quality
package:

### Tier 1

* README file preferably with the following information:
  * overview of what functionality this package provides
  * basic usage examples
  * installation process
    * native libraries that this code wraps
    * any special tools needed
  * caveats
* test suite to check if the package works as expected with the latest stable
  Janet release. Tests are also a great way to explore the package API.

### Tier 2:

* example files that are easy to follow and shows usage of the package code.
* `CONTRIBUTING` file similar to this one.

### Tier 3:

* `TECH` file with details about implementation and inner workings of the package.


## Broken links

Please open issues if you find broken links in the package listing here. Try to find the correct link or at least
the reason for a link breakage. We can then update or remove offending packages.
