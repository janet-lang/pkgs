# Guidelines for contributing to the Janet Package Listing

Thanks for taking the time to contribute!

Please read this document before making contributions. If you find anything
missing of not appropriate, please do not hesitate and create an issue in this
repository.

## Adding a Package

If you would like to add a package here, open a pull request with the
package's name and URL and edit the pkgs.janet file. Plus points for simple
descriptions or reasons why you are adding the package in the comment.

These are essential requirements on the package. The
probability of merge correlates with completeness.

* Check if the package exists before adding it twice.
* Make sure that users can use your package with `jpm`. It must have a file
  `project.janet` in its root directory and properly run when installed via
  `jpm install https://some.git-host.org/me/mypackage.git`. Do not add
  packages that do not work with jpm! If jpm cannot support your package,
  open an issue in this repository, and we will see what we can do.
* Please be sure that your `project.janet` file contains these required fields:
  * `:name` with the desired name of the package. The package's name should
  usually be the same as its git repository and should be all lower case
  and in kebab-case.
    * Good package names.
      * `my-package`
      * `thing`
      * `thing@bakpakin` (for a fork of the package)
    * Bad package names
      * `mypackage`
      * `my_package`
      * `MyPackage`
      * `my package`
      * `my.package.git`
      * `org.this.is.not.java.AbstractWidgetFactoryProducer`
  *  `:author` name of the author of the package. Preferably with email contact
  in the standard format: `"Josef Pospíšil <josef.pospisil@laststar.eu>"`.
  * `:description` short informative description of the package, preferably one
  sentence.
  * `:license` abbreviation of the License name, e.g., "MIT".
  * `:url` with further information about the package. It could be a repository
  home page with `README.md` or any other website.
  * `:repo` from which users could clone code.
  * `:dependencies` field is optional but must be present if it depends on
  other packages.
* Add package License, preferably in the LICENSE file in the root of the
  project.


## Optional Package properties

These are not required (at least for now) but are nice to have for any quality
package:

### Tier 1

* README file preferably with following information:
  * basic usage examples
  * installation process
    * native libraries code wraps
    * special tools needed
  * caveats
* test suite to check if the package works as expected with the latest stable
  Janet release. Tests are also a great way to explore the package API.

### Tier 2:

* example files that are easy to follow and shows usage of the package code.
* CONTRIBUTING file similar to this.

### Tier 3:

* TECH file with details about implementation and inner working of the package.


## Broken Links

Please open issues if you find broken links. Try to find the correct link or at least
the reason for a link breakage. We can then update or remove offending packages.
