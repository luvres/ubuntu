### Ubuntu Slim
#### Reference: (https://hub.docker.com/_/ubuntu/)
```
mkdir ROOTFS
mv ubuntu-xenial-core-cloudimg-amd64-root.tar.gz ROOTFS
cd ROOTFS
sudo tar zxf ubuntu-xenial-core-cloudimg-amd64-root.tar.gz
sudo rm usr/share/doc/* usr/share/locale/* usr/share/man/* usr/share/info/* usr/share/lintian/* *.tar.gz -fR
sudo tar zcf ubuntu-xenial-core-cloudimg-amd64-root.tar.gz *
mv ubuntu-xenial-core-cloudimg-amd64-root.tar.gz ..
cd ..
sudo chown -R $USER. ubuntu-xenial-core-cloudimg-amd64-root.tar.gz
sudo rm ROOTFS/ -fR
```
#### Build
```
docker build -t izone/ubuntu:xenial-slim ./xenial-slim/
```

