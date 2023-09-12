# Streaming Steamdeck to OBS

## RTMP Streaming

This will setup an rtmp webserver on your computer that the steamdeck can stream it's screen to. No need for capture cards or other kind of cables. This only works for the gamemode of the steamdeck. I currently do not have a setup to stream desktop mode.

### Prerequisites

#### Steamdeck

- Login to steamdeck via [SSH](ssh.md)
- Install the packages below

```
sudo steamos-readonly disable
sudo pacman -S gst-plugins-ugly gst-plugins-bad gstreamer-vaapi gst-plugin-pipewire gst-plugins-good gst-libav gst-plugins-base gst-plugins-good gstreamer-vaapi gst-plugin-pipewire
sudo steamos-readonly enable
```

#### Remote machine

- Have docker available
- Know IP of the machine so you can replace `<docker_container_host_ip>` on the steamdeck command and the OBS media source
- Run below command

```
docker run -d -p 1935:1935 --name rtmp-stream alfg/nginx-rtmp
```

### Streaming steamdeck to RTMP

<img src="https://imgur.com/L513f2y.png" />
RTMP Streaming from the steamdeck via ssh

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
        ! rtmpsink location='rtmp://<docker_container_host_ip>:1935/stream/deck live=1'
```

### OBS

<img src="https://i.imgur.com/aVZNz5y.png" />
The OBS media source settings

- Add a media source to OBS with the url `rtmp://<docker_container_host_ip>:1935/stream/deck`
- ???
- Profit.

## Capture card

Stuff goes here
