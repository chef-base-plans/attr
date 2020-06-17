[![Build Status](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_apis/build/status/chef-base-plans.attr?branchName=master)](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_build/latest?definitionId=69&branchName=master)

# attr

## Maintainers

* The Habitat Maintainers: <humans@habitat.sh>

## Type of Package

Binary package

## Usage

```bash
$ hab pkg install core/attr --binlink
$ attr --help
attr: invalid option -- '-'
Unrecognized option: ?
Usage: attr [-LRSq] -s attrname [-V attrvalue] pathname  # set value
       attr [-LRSq] -g attrname pathname                 # get value
       attr [-LRSq] -r attrname pathname                 # remove attr
       attr [-LRq]  -l pathname                          # list attrs 
      -s reads a value from stdin and -g writes a value to stdout
[20][default:/src:1]# getfattr --help
getfattr 2.4.48 -- get extended attributes
Usage: getfattr [-hRLP] [-n name|-d] [-e en] [-m pattern] path...
  -n, --name=name         get the named extended attribute value
  -d, --dump              get all extended attribute values
  -e, --encoding=...      encode values (as 'text', 'hex' or 'base64')
      --match=pattern     only get attributes with names matching pattern
      --only-values       print the bare values only
  -h, --no-dereference    do not dereference symbolic links
      --absolute-names    don't strip leading '/' in pathnames
  -R, --recursive         recurse into subdirectories
  -L, --logical           logical walk, follow symbolic links
  -P  --physical          physical walk, do not follow symbolic links
      --version           print version and exit
      --help              this help text
$ setfattr --help
setfattr 2.4.48 -- set extended attributes
Usage: setfattr {-n name} [-v value] [-h] file...
       setfattr {-x name} [-h] file...
  -n, --name=name         set the value of the named extended attribute
  -x, --remove=name       remove the named extended attribute
  -v, --value=value       use value as the attribute value
  -h, --no-dereference    do not dereference symbolic links
      --restore=file      restore extended attributes
      --raw               attribute value is not encoded
      --version           print version and exit
      --help              this help text
$ 
```
