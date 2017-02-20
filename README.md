# up
A script for moving up directories quickly.

# Usage

```shell
# Move up one directory. Equivalent to: cd ..
up
up 1

# Move up two directories. Equivalent to cd: ../..
up 2

# Move up four directories and into a meetings folder.
# Equivalent to: cd ../../../../meetings
up 4 meetings
```

# Installation

Place the `_up` script in a directory that is on your `PATH`; e.g. `~/bin`

Create an alias in the following format: `alias up=". _up"`

# Quirks

The script fails in the scenario where a directory is simply named with a number:

```shell
| parent-dir/
\ - 9/
\ - some-dir/

# If you're in some-dir/ trying to get to 9/,
# this fails by taking you up 9 directories instead.
up 9

# To avoid this, try one of the following:
up 1 9
up ./9
```

# License

[MIT](LICENSE)
