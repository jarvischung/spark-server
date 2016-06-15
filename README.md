# spark-server
Support Particle device and use docker solution.

# How to use:
```
docker pull jarvischung/spark-server
```
```
docker run -it -p 8080:8080 "jarvischung/spark-server:v1.0.0"
```
Note: Spark-Server will use 8080 port.

If the container is running, you can get server key from console. Please save the key.
Just like:
```
........
Loading server key from default_key.pem
set server key
server public key is:  -----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAzmAWMFQ3VZZCWvOnY+Kd
S9GBJPOntsWrQAKiuIGAqmTolp7F8DycVUMnLm3Eijr0JvGrFW6/uzzX5Tj+K7Lw
e15AKi+kbVzuaQGZeZmPH3KmtjAG9KEcx6FuFIipBcvSz7/wLJSoxo1IS2lk03Wu
JZsiRllLkU8RQRk/F4cndzfLN0xj2Sti7Y8AgWBirKQJbwq8wqdufr2aDsb6RiFY
Ok6qOVHj81dPd/me+VK0BZlc0KV0IVcORwnARUStbTGDdxlvtsg5DoG98JAT0HxI
4sGTIamH5qlvSMScq2hB0MWZtnBI/aleOD97b95JZUfbp5JlpM6L1mwyacsH1sV6
WwIDAQAB
-----END PUBLIC KEY-----

```

# Related information:

https://www.particle.io/

https://hub.docker.com/r/jarvischung/spark-server-docker/

https://github.com/spark/spark-server
