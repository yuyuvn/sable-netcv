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

### Dependencies

http://blog.mycodesite.com/compile-opencv-with-ffmpeg-for-ubuntudebian/

https://launchpad.net/~mc3man/+archive/ubuntu/trusty-media

### TODO:
* ~~use h.264 to compress data before stream. Change h.264 quality depend on tested data. (quality is set offline).~~
* ~~detect busy and frameskip (may create more socket connection)~~
* ~~Crop and tranform webcame resolution to 320x240~~
* ~~Change tcp to udp~~

* May change to ffmpeg lib instead of opencv
 
## Update:
Use ffmpeg (client use C++ for dangerous)

Command line example:

Client:
```ffmpeg -f v4l2 -i "/dev/video0" -r 50 -vcodec mpeg2video -b:v 1000k -f mpegts tcp://127.0.0.1:12345```

Server:
```ffplay tcp://0.0.0.0:12345?listen -analyzeduration 500```

### TODO:
* Use ffmpeg c++ api to receive webcam frame (from v4l2 driver) then stream via tcp.
