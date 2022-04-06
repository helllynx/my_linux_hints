# EndeavourOS

If after update u see:

```shell
error: GPGME error: No data
error: GPGME error: No data
error: GPGME error: No data
error: failed to synchronize all databases (unexpected error)
```

At first remove db:

```shell
sudo pacman -Scc
```

if it not helped

```
sudo pacman-key --lsign-key EndeavourOS
sudo pacman -S endeavouros-keyring
```

then update again.
