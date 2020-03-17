# redo-c
Arch User Repository redo-c - An implementation of the redo build system in portable C with zero dependencies

## Update package

* Update package version in PKGBUILD
* Generate new checksums with

```$ updpkgsums```

* Test install

```$ makepkg -si```

* Update .SRCINFO 

```$ makepkg --printsrcinfo > .SRCINFO```
