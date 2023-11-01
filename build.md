# How to build

```sh
shfmt -w PKGBUILD && updpkgsums && makepkg --printsrcinfo > .SRCINFO && makepkg  -C -sfi && namcap *.zst
```

> fmt PKGBUILD, update checksum, update .SRCINFO, (re)build package, install, test the package.
