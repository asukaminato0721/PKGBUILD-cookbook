# 

automatically get all the depends by namcap

```sh
namcap *.pkg.tar.zst | grep --perl-regexp 'ency .*? detected' --only-matching | cut --delimiter=' ' --fields=2
```

then copy the output to PKGBUILD
