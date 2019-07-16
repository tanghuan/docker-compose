# docker-compose
快速搭建各种服务


# rtmp
推流：ffmpeg -re -i 视频地址 -vcodec libx264 -acodec aac -f flv rtmp://{ip}:{port}/stream/{stream-name}
ffmpeg -re -i /root/test.mp4 -vcodec libx264 -acodec aac -f flv rtmp://localhost:1935/stream/hello

拉流：rtmp://{ip}:{port}/stream/{stream-name}
rtmp://192.168.3.25:1935/stream/hello

hls播放：http://ip:port/live/{stream-name}.m3u8
http://192.168.3.25:8100/live/hello.m3u8
