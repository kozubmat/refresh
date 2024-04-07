# Backup WSL
```shell
mkdir D:\backup
wsl --export Ubuntu D:\backup\ubuntu.tar
```

# Deregister WSL
```shell
wsl --unregister Ubuntu
```

# Import WSL in another location
```shell
mkdir D:\wsl
wsl --import Ubuntu D:\wsl\ D:\backup\ubuntu.tar
```
