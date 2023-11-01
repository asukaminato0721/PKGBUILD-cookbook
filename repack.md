# repack

repack from deb

```sh
bsdtar -xvf data.tar.* -C "$pkgdir"
```

> use * to match gz / bz / bz2 / xz / zst

______________________________________________________________________

repack from pacman

```sh
rm *.pkg.tar.zst
cp -av * "$pkgdir"
```

attention:

glob has some strange effect. <https://superuser.com/questions/1618470/shell-globbing-doesnt-work-the-way-i-expect>

so if not sure, use `find + op`
