# Streaming Steamdeck to OBS

## RTMP

Run docker container on remote machine to relay the rtmp stream

```
docker run -d -p 1935:1935 --name rtmp-stream alfg/nginx-rtmp
```

Login to the steamdeck through ssh, and run the following

```
gst-launch-1.0 -e \
    pipewiresrc do-timestamp=True \
        ! queue \
        ! videoconvert \
        ! queue \
        ! vaapih264enc \
        ! h264parse \
        ! mux. \
    pulsesrc device="alsa_output.pci-0000_04_00.5-platform-acp5x_mach.0.HiFi__hw_acp5x_1__sink.monitor" \
        ! queue \
        ! fdkaacenc bitrate=320000 \
        ! mux. \
    flvmux name=mux streamable=True \
        ! rtmpsink location='rtmp://<docker_container_host_ip>:11935/stream/deck live=1'
```

Now add a media thing to OBS with the url `rtmp://<docker_container_host_ip>:11935/stream/deck`
