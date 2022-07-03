# video_stream_udp
For transmission of video feeds wirelessly over long distance using a USB camera.



Protocol used: <b>UDP</b>

#### On server (host computer(base station) - where video feed is viewed)
##### Figure out the host IP address
```
ifconfig
```
For example, IP is 192.168.1.10 over wlan0

Then this is the host IP address

```
python3 udp_server.py <host_ip> <port>
```
#### On client (computer on which the cameras are connected)
Source number is the index of the camera connected.

if 1 camera connected then available sources - 0

if 2 camera connected then available sources - 0, 1 and so on
```
python3 udp_client.py <host_ip> <port> <source_number>
```

Repeat the same process for getting simultaneous feed from different cameras. Change source number according to the camera.
