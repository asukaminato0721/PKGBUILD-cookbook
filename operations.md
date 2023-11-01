# operations

ref <https://unix.stackexchange.com/questions/104982/why-use-install-rather-than-cp-and-mkdir>

## create dir

```sh
install -d x/y/z
```

why not `mkdir -p`

<https://unix.stackexchange.com/questions/340169/whats-the-difference-between-mkdir-p-and-install-d>

## put file

non-executable file

```sh
install -vDm644 $srcdir/<src> [-t] $pkgdir/<dst>
```

executable file

```sh
install -vDm755 $srcdir/<src> [-t] $pkgdir/<dst>
```

desktop file

```sh
find $srcdir \
 -name "*.desktop" \
 -print \
 -exec install -Dm644 {} -t "$pkgdir/usr/share/applications/" \;
```

______________________________________________________________________

## remove file

remove electron files

```sh
find "$pkgdir/opt" -not -path "*/resources/*" -type f -delete
```

remove empty folders

```sh
find "$pkgdir" -type d -empty -delete
```

<https://unix.stackexchange.com/questions/8430/how-to-remove-all-empty-directories-in-a-subtree>
