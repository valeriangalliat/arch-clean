Arch Clean
==========

> Clean packages on an Arch Linux system.

Overview
--------

This little script will help you remove unneeded packages from your
Arch Linux installation.

It will find *all explicitely installed packages*, exclude packages from
`base` and `base-devel`, exclude packages from an optional `kp`
*(keep)* file, then prompt you with this list.

You then *let in the list all the packages you don't want anymore*.
All the packages you removed from the list will be added to the `kp`
file so you won't be prompted about them on the next run.

When you finished editing, the packages in the list are removed
recursively (with their dependencies).

At the end, all orphan packages are also removed.

Installation
------------

```sh
git clone https://github.com/valeriangalliat/arch-clean.git
```

Usage
-----

```sh
cd arch-clean
./arch-clean
```

**Note:** all the temporary files are created in the current working
directory, so it's better to `cd` first.
