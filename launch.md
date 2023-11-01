# launch

electron launch script

```sh
printf "#!/bin/sh
exec electron /opt/$pkgname/xxx \"\$@\"
" | install -Dm755 /dev/stdin "$pkgdir/usr/bin/xxx"
```

why `printf` instead of `echo -e`

<https://unix.stackexchange.com/questions/65803/why-is-printf-better-than-echo>

why not `install -Dm755 <(printf "xx") `

<https://github.com/fish-shell/fish-shell/issues/5181>

why use `exec`

<https://stackoverflow.com/questions/18351198/what-are-the-uses-of-the-exec-command-in-shell-scripts>

what is `$@`

<https://stackoverflow.com/questions/9994295/what-does-mean-in-a-shell-script>
