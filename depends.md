# 

automatically get all the depends by namcap

```sh
namcap *.pkg.tar.zst | grep --perl-regexp 'ency .*? detected' --only-matching | cut --delimiter=' ' --fields=2
```

then copy the output to PKGBUILD

---

check electron version

for windows electron app

```sh
strings *.exe | grep '^Chrome/[0-9.]* Electron/[0-9]'
```

for linux

```sh
strings <app> | grep '^Chrome/[0-9.]* Electron/[0-9]'
```
