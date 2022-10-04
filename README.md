# Notes from Xchwarze

This project is copy of https://github.com/xchwarze/wifi-pineapple-cloner/

Uses:
* The method that releases in 2021
* My cracked binaries
* The script I made for my tetra 20-sd-tetra-fix
* It even has the same mistakes I made 🤣

If you were going to port my work at least you should have given me credit.
Especially if when you diff it you see that it is exactly the same even in the errors.


# Sweet WiFi Pineapple Tetra Builder

Sweet Pineapple Builder is a python script that automate the whole process of creating a custom WiFi Pineapple Tetra image. As the WiFi Pineapple Tetra firmware is a custom version of OpenWrt (19.07.2), it is therefore possible to create our own custom firmware tailored to any router based on the MIPS 24Kc architecture.<br><br>
Full blog post for more details: [https://samy.link/blog/build-your-own-wifi-pineapple-tetra-for-7](https://samy.link/blog/build-your-own-wifi-pineapple-tetra-for-7)

![WiFi pineapple DIY Logo](https://raw.githubusercontent.com/Nwqda/Sweet-Pineapple-Builder/master/cake/seed/Sweet-bg.jpeg)


### Supported devices

For now the script only support the following routers:

Brand       | Device         | CPU (MHZ)         | Flash MB| RAM MB | More info|
-------------|-------------| -----------| -----------| -----------| -----------|
HAK5  | Pineapple Tetra | 580 |32 + 2GB eMMC|64|https://openwrt.org/toh/hwdata/hak5/hak5_wifi_pineapple_mark_7
Buffalo  | WZR450HP2 | 400 |32|64|https://openwrt.org/toh/buffalo/wzr-450hp2
Buffalo  | WZR600DHP | 680 |32|128|https://openwrt.org/toh/hwdata/buffalo/buffalo_wzr-600dhp
Buffalo  | WZRHPAG300H | 680 |32|128|https://openwrt.org/toh/hwdata/buffalo/buffalo_wzr-hp-ag300h_v1
Buffalo  | WZRHPG300NH | 400 |32|64|https://openwrt.org/toh/hwdata/buffalo/buffalo_wzr-hp-g300nh_v1
Buffalo  | WZRHPG300NH2 | 400 |32|64|https://openwrt.org/toh/hwdata/buffalo/buffalo_wzr-hp-g300nh2_v2
Buffalo  | WZRHPG450H | 400 |32|64|https://openwrt.org/toh/hwdata/buffalo/buffalo_wzr-hp-g450h_v1
D-Link   | DGL5500A1 | 720 |16|128|https://openwrt.org/toh/hwdata/d-link/d-link_dgl-5500_a1
D-Link   | DIR835A1 | 560 |16|128|https://openwrt.org/toh/d-link/dir-835_a1
D-Link   | dir-869-a1 | 750 |16|64|https://openwrt.org/toh/hwdata/d-link/d-link_dir-869_a1
GL.iNet  | gl-ar300 | 560 |16|128|https://openwrt.org/toh/hwdata/gl.inet/gl.inet_gl-ar300
GL.iNet  | gl-ar300m | 650 |16|128|https://openwrt.org/toh/gl.inet/gl-ar300m
GL.iNet  | gl-ar750 | 650 |16|128|https://openwrt.org/toh/hwdata/gl.inet/gl.inet_gl-ar750
GL.iNet  | gl-ar750s | 775 |16|128|https://openwrt.org/toh/hwdata/gl.inet/gl.inet_gl-ar750s
TP-Link  | archer-c7-v2 | 720 |16|128|https://openwrt.org/toh/hwdata/tp-link/tp-link_archer_c7_ac1750_v2.0
TP-Link  | archer-c7-v4 | 775 |16|128|https://openwrt.org/toh/hwdata/tp-link/tp-link_archer_c7_v4
TP-Link  | archer-c7-v5 | 750 |16|128|https://openwrt.org/toh/hwdata/tp-link/tp-link_archer_c7_v5
<br>
PS: Let me know if you want me to add more routers. 

### Requirement
-   Ubuntu/Debian (Tested with Ubuntu 22.04)
-   Python 3 (Tested with Python 3.10.4)
-   A router from the list above. (Make sure OpenWrt 19.07.2 has been already install on the device).

### Installation

Clone this repository and run:
```shell
pip install -r requirements.txt
```

#### Usage
```shell
python3 sweetPineappleBuilder.py 
```
Then select your router from the list and that's all.<br>
Now, be patient for around 10 minutes to complete the download and compilation process.<br><br>
![WiFi pineapple DIY](https://raw.githubusercontent.com/Nwqda/Sweet-Pineapple-Builder/master/cake/seed/Sweet-screenshot.png)
<br>

### Docker
To make things even simpler, I also created a docker image with the tool and all OpenWrt packages already pre-installed, ~1.4GB.<br>
To use it, just run:

```bash
docker pull naqwada/sweetpineapplebuilder
docker run -dit naqwada/sweetpineapplebuilder sleep infinity
docker ps -a
docker exec -it <CONTAINER ID> /bin/bash
cd /home/Sweet-Pineapple-Builder
python3 sweetPineappleBuilder.py
```


### Proof Of Concept / Tutorial
[![Video PoC WiFI Pineapple Tetra DIY](https://i.ibb.co/7gXHL9q/500px-youtube-social-play.png)](https://www.youtube.com/watch?v=RrzqmJnzbA4)


### Note
If you have difficulties to compile the image you can check out my blog post ([https://samy.link/blog/build-your-own-wifi-pineapple-tetra-for-7](https://samy.link/blog/build-your-own-wifi-pineapple-tetra-for-7)) or create a ticket in the "issue" tab and I will try to help.
