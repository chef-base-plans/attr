[![Build Status](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_apis/build/status/chef-base-plans.attr?branchName=master)](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_build/latest?definitionId=69&branchName=master)

# attr

The attr package contains utilities to administer the extended attributes on filesystem objects.  See [documentation](http://www.linuxfromscratch.org/lfs/view/stable/chapter06/attr.html)

## Maintainers

* The Core Planners: <chef-core-planners@chef.io>

## Type of Package

Binary package

### Use as Dependency

Binary packages can be set as runtime or build time dependencies. See [Defining your dependencies](https://www.habitat.sh/docs/developing-packages/developing-packages/#sts=Define%20Your%20Dependencies) for more information.

To add core/attr as a dependency, you can add one of the following to your plan file.

##### Buildtime Dependency

> pkg_build_deps=(core/attr)

##### Runtime dependency

> pkg_deps=(core/attr)

### Use as Tool

#### Installation

To install this plan, you should run the following commands to first install, and then link the binaries this plan creates.

``hab pkg install core/attr --binlink``

will add the following binaries to the PATH:

* /bin/attr
* /bin/getfattr
* /bin/setfattr

#### Using an example binary

You can now use the binary as normal.  For example:

``/bin/getfattr --help`` or ``getfattr --help``

```bash
getfattr --help
getfattr 2.4.48 -- get extended attributes
Usage: getfattr [-hRLP] [-n name|-d] [-e en] [-m pattern] path...
  -n, --name=name         get the named extended attribute value
  -d, --dump              get all extended attribute values
  -e, --encoding=...      encode values (as 'text', 'hex' or 'base64')
      --match=pattern     only get attributes with names matching pattern
      --only-values       print the bare values only
...
...
```
