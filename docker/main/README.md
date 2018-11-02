
To build Main_Mister, do the following:

1) Install Docker

2) (optional) Put `mm` script in your path somewhere
```
cp mm ~/.bin
export PATH=~/.bin/:$PATH
```

3) Pull down the OpenVGS linaro toolchain
```
docker pull openvgs/linaro
```

4) Checkout Main_Mister
```
git clone https://github.com/MiSTer-devel/Main_MiSTer.git
```

5) Build Main_Mister
```
mm make
```

Alterative to 5) Run docker explicitly (this is all `mm` is)
```
docker run --rm -it -v $(pwd):/source openvgs/linaro:latest make
```


Note
----
This is just a thin layer over the wsbu/linaro-toolchain container. Thanks, linaro guys.
