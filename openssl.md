# OpenSSL
## Symetric encryption with openssl
### Encrypt:
```
openssl aes-256-cbc -a -salt -in secrets.txt -out secrets.txt.enc
```

### Decrypt:
```
openssl aes-256-cbc -d -a -in secrets.txt.enc -out secrets.txt.new
```

## Check if a SSL/TLS certificate certificate is valid
```
openssl s_client -showcerts -connect www.example.com:443
```
