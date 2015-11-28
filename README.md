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
* use x264 to compress data before stream. Change x264 quality depend on tested data. (quality is set offline).
* detect busy and frameskip (may create more socket connection)
* Crop and tranform webcame resolution to 320x240
* Change tcp to udp

