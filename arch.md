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

if it not helped edit `/etc/pacman.conf` change `SigLevel` to `Required DatabaseNever`

```
SigLevel    = Required DatabaseNever
```

then

```
sudo pacman-key --lsign-key EndeavourOS
sudo pacman -S endeavouros-keyring
```

then update again and don't forget to revert `SigLevel` in `/etc/pacman.conf` back to `DatabaseOptional`.
