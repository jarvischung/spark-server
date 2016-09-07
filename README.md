# spark-server
Support Particle device and use docker solution.

# How to use:
```
docker pull jarvischung/spark-server:v1.0.0
```
or
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
# How to modify server address:
Step 1: Saved your server key(default_key.pem).

Step 2: To enter DFU mode.

Device modes: https://docs.particle.io/guide/getting-started/modes/photon/

Step 3: Upload key to your Particle device 
```
  # particle keys server *.pub.pem 127.0.0.1
```
Step 4: Create a profile for your server
```
  # particle config particle-local apiUrl http://127.0.0.1:8080  (don’t append “/”)
  # particle config useSudoForDfu true
  # particle config identify
```
Step 5: Create a user for login
```
  # particle login
```
Step 6: Get your device id (LISTENING MODE)
```
  # particle identify
  Your device id is 220XXXXXXX3737XXXXXXXXX
  Your system firmware version is 0.6.0
```
Setp 7: Created a new device key
```
  # particle keys doctor 220XXXXXXX3737XXXXXXXXX
```
or Get device key for your Particle device
```
  # particle keys save 220XXXXXXX3737XXXXXXXXX
```
Step 8: Send your device to your server
```
  # particle keys send 220XXXXXXX3737XXXXXXXXX 220XXXXXXX3737XXXXXXXXX.pub.pem
```
Step 9: Complie your code and flash your program to your device
```
  # particle compile photon test.ino --saveTo firmware.bin
  # particle flash 220XXXXXXX3737XXXXXXXXX firmware.bin
```

enjoy!!

# Related information:

https://www.particle.io/

https://hub.docker.com/r/jarvischung/spark-server-docker/

https://github.com/spark/spark-server
