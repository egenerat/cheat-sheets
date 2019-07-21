## Compression/extraction

### Create an archive
```
tar -zcvf archive.tar.gz folder
```

### Uncompress
```
tar -zxvf archive.tar.gz
```

Even possible without `z`, in that case it recognizes the format of the archive itself
```
tar xf archive.tar.xz
```
