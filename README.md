# sable-netcv

Compile:
```
cd server
cmake .
make
cd ../client
cmake .
make
```

install Dependencies:

http://blog.mycodesite.com/compile-opencv-with-ffmpeg-for-ubuntudebian/

https://launchpad.net/~mc3man/+archive/ubuntu/trusty-media

TODO:
* use h.264 to compress data before stream. Change h.264 quality depend on tested data. (quality is set offline). If there are 3/4 allocated time remains, find a simple way to compress mat data (jpeg, pca...)
* detect busy and frameskip (may create more socket connection)
* Crop and tranform webcame resolution to 320x240
* Change tcp to udp

* May change to ffmpeg lib instead of opencv
