  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE

Run 'docker image COMMAND --help' for more information on a command.
[node1] (local) root@192.168.0.8 ~
$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
busybox       latest    42b97d3c2ae9   3 days ago     1.24MB
nginx         latest    dd34e67e3371   6 days ago     133MB
hello-world   latest    d1165f221234   5 months ago   13.3kB
[node1] (local) root@192.168.0.8 ~
$ docker run debian
Unable to find image 'debian:latest' locally
latest: Pulling from library/debian
4c25b3090c26: Pull complete 
Digest: sha256:38988bd08d1a5534ae90bea146e199e2b7a8fca334e9a7afe5297a7c919e96ea
Status: Downloaded newer image for debian:latest
[node1] (local) root@192.168.0.8 ~
$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
busybox       latest    42b97d3c2ae9   3 days ago     1.24MB
nginx         latest    dd34e67e3371   6 days ago     133MB
debian        latest    fe3c5de03486   7 days ago     124MB
hello-world   latest    d1165f221234   5 months ago   13.3kB
[node1] (local) root@192.168.0.8 ~
$ dock
docker                 docker-entrypoint.sh   docker-prompt          dockerd                
docker-compose         docker-init            docker-proxy           dockerd-entrypoint.sh  
[node1] (local) root@192.168.0.8 ~
$ docker start ^Cte
[node1] (local) root@192.168.0.8 ~
$ history 
    1  ls
    2  git clone htts://github.com/luistkd4/docker101
    3  git clone https://github.com/luistkd4/docker101
    4  ls
    5  cd docker101/
    6  cd IntroComands/
    7  ls
    8  vim principais_comandos.sh 
    9  cat I
   10  cat principais_comandos.sh 
   11  wget https://github.com/wagoodman/dive/releases/download/v0.9.2/dive_0.9.2_linux_amd64.deb
   12  sudo apt install ./dive_0.9.2_linux_amd64.deb
   13  cd
   14  sudo su 
   15  docker run --name newcontainer hello-world
   16  docker run --name hello -d buybox sleep 3600
   17  docker run --name hello -d busybox sleep 3600
   18  docker ps
   19  docker run --name site -d -p 80:80 nginx
   20  docker ps
   21  curl nginix
   22  curl nginx
   23  curl localhost
   24  netstat -nltp
   25  man curl
   26* 
   27  docker ps
   28  docker ls
   29  docker -a
   30  docker ps
   31  docker ps -a
   32  docker ps
   33  docker exec hello mkdir teste
   34  docker exec -it hello sh 
   35  docker stop site
   36  docker ps
   37  curl localhost
   38  netstat -nltp
   39  docker start site
   40  curl localhost
   41  netstat -nltp
   42  docker logs site
   43  docker logs site
   44  docker image
   45  docker images
   46  docker run debian
   47  docker images
   48  history 
[node1] (local) root@192.168.0.8 ~
$ docker run --name debian debian
[node1] (local) root@192.168.0.8 ~
$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
busybox       latest    42b97d3c2ae9   3 days ago     1.24MB
nginx         latest    dd34e67e3371   6 days ago     133MB
debian        latest    fe3c5de03486   7 days ago     124MB
hello-world   latest    d1165f221234   5 months ago   13.3kB
[node1] (local) root@192.168.0.8 ~
$ dock
docker                 docker-entrypoint.sh   docker-prompt          dockerd                
docker-compose         docker-init            docker-proxy           dockerd-entrypoint.sh  
[node1] (local) root@192.168.0.8 ~
$ docker start debian
debian
[node1] (local) root@192.168.0.8 ~
$ docker start debian -it bash
[node1] (local) root@192.168.0.8 ~
$ dock
docker                 docker-entrypoint.sh   docker-prompt          dockerd                
docker-compose         docker-init            docker-proxy           dockerd-entrypoint.sh  
[node1] (local) root@192.168.0.8 ~
$ docker run -it -d ubuntu /bin/bash
Unable to find image 'ubuntu:latest' locally
latest: Pulling from library/ubuntu
16ec32c2132b: Pull complete 
Digest: sha256:82becede498899ec668628e7cb0ad87b6e1c371cb8a1e597d83a47fac21d6af3
Status: Downloaded newer image for ubuntu:latest
5a004080b69a5c9e9af2ca8eee2bf98dcfeb96c6bed2b205cfc5abda993c77a8
[node1] (local) root@192.168.0.8 ~
$ dock
docker                 docker-entrypoint.sh   docker-prompt          dockerd                
docker-compose         docker-init            docker-proxy           dockerd-entrypoint.sh  
[node1] (local) root@192.168.0.8 ~
$ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS                NAMES
5a004080b69a   ubuntu    "/bin/bash"              21 seconds ago   Up 20 seconds                        laughing_napier
c8701915f8cd   nginx     "/docker-entrypoint.…"   48 minutes ago   Up 10 minutes   0.0.0.0:80->80/tcp   site
5cd87c94b895   busybox   "sleep 3600"             49 minutes ago   Up 49 minutes                        hello
[node1] (local) root@192.168.0.8 ~
$ dock
docker                 docker-entrypoint.sh   docker-prompt          dockerd                
docker-compose         docker-init            docker-proxy           dockerd-entrypoint.sh  
[node1] (local) root@192.168.0.8 ~
[node1] (local) root@192.168.0.8 ~
$ docker run ubuntu -it ubuntu bash
[node1] (local) root@192.168.0.8 ~
$ docker run --name ubuntinho -it ubuntu bash
root@675d5758f359:/# apt update
Get:1 http://security.ubuntu.com/ubuntu focal-security InRelease [114 kB]
Get:2 http://archive.ubuntu.com/ubuntu focal InRelease [265 kB]          
Get:3 http://security.ubuntu.com/ubuntu focal-security/multiverse amd64 Pa
ckages [30.6 kB]
Get:4 http://security.ubuntu.com/ubuntu focal-security/universe amd64 Pack
ages [792 kB]
Get:5 http://security.ubuntu.com/ubuntu focal-security/restricted amd64 Pa
ckages [488 kB]
Get:6 http://security.ubuntu.com/ubuntu focal-security/main amd64 Packages
 [1034 kB]
Get:7 http://archive.ubuntu.com/ubuntu focal-updates InRelease [114 kB]  
Get:8 http://archive.ubuntu.com/ubuntu focal-backports InRelease [101 kB]
Get:9 http://archive.ubuntu.com/ubuntu focal/multiverse amd64 Packages [17
7 kB]
Get:10 http://archive.ubuntu.com/ubuntu focal/universe amd64 Packages [11.
3 MB]
Get:11 http://archive.ubuntu.com/ubuntu focal/main amd64 Packages [1275 kB
]
Get:12 http://archive.ubuntu.com/ubuntu focal/restricted amd64 Packages [3
3.4 kB]
Get:13 http://archive.ubuntu.com/ubuntu focal-updates/restricted amd64 Pac
kages [534 kB]
Get:14 http://archive.ubuntu.com/ubuntu focal-updates/multiverse amd64 Packages [33.8 kB]
Get:15 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 Packages [1471 kB]
Get:16 http://archive.ubuntu.com/ubuntu focal-updates/universe amd64 Packages [1065 kB]
Get:17 http://archive.ubuntu.com/ubuntu focal-backports/universe amd64 Packages [6324 B]
Get:18 http://archive.ubuntu.com/ubuntu focal-backports/main amd64 Packages [2668 B]
Fetched 18.9 MB in 3s (7229 kB/s)                
Reading package lists... Done
Building dependency tree       
Reading state information... Done
4 packages can be upgraded. Run 'apt list --upgradable' to see them.
root@675d5758f359:/# sudo apt install neofetch
bash: sudo: command not found
root@675d5758f359:/# apt install neofetch
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  chafa dbus fontconfig-config fonts-dejavu-core fonts-droid-fallback fonts-noto-mono fonts-urw-base35 ghostscript
  gsfonts imagemagick-6-common krb5-locales libapparmor1 libavahi-client3 libavahi-common-data libavahi-common3
  libbsd0 libchafa0 libcups2 libdbus-1-3 libexpat1 libfftw3-double3 libfontconfig1 libfreetype6 libglib2.0-0
  libglib2.0-data libgomp1 libgs9 libgs9-common libgssapi-krb5-2 libicu66 libidn11 libijs-0.35 libjbig0 libjbig2dec0
  libjpeg-turbo8 libjpeg8 libk5crypto3 libkeyutils1 libkrb5-3 libkrb5support0 liblcms2-2 liblqr-1-0 libltdl7
  libmagickcore-6.q16-6 libmagickwand-6.q16-6 libopenjp2-7 libpaper-utils libpaper1 libpng16-16 libssl1.1 libtiff5
  libwebp6 libwebpmux3 libx11-6 libx11-data libxau6 libxcb1 libxdmcp6 libxext6 libxml2 poppler-data shared-mime-info
  tzdata ucf xdg-user-dirs
Suggested packages:
  default-dbus-session-bus | dbus-session-bus fonts-noto fonts-freefont-otf | fonts-freefont-ttf fonts-texgyre
  ghostscript-x cups-common libfftw3-bin libfftw3-dev krb5-doc krb5-user liblcms2-utils libmagickcore-6.q16-6-extra
  poppler-utils fonts-japanese-mincho | fonts-ipafont-mincho fonts-japanese-gothic | fonts-ipafont-gothic
  fonts-arphic-ukai fonts-arphic-uming fonts-nanum
The following NEW packages will be installed:
  chafa dbus fontconfig-config fonts-dejavu-core fonts-droid-fallback fonts-noto-mono fonts-urw-base35 ghostscript
  gsfonts imagemagick-6-common krb5-locales libapparmor1 libavahi-client3 libavahi-common-data libavahi-common3
  libbsd0 libchafa0 libcups2 libdbus-1-3 libexpat1 libfftw3-double3 libfontconfig1 libfreetype6 libglib2.0-0
  libglib2.0-data libgomp1 libgs9 libgs9-common libgssapi-krb5-2 libicu66 libidn11 libijs-0.35 libjbig0 libjbig2dec0
  libjpeg-turbo8 libjpeg8 libk5crypto3 libkeyutils1 libkrb5-3 libkrb5support0 liblcms2-2 liblqr-1-0 libltdl7
  libmagickcore-6.q16-6 libmagickwand-6.q16-6 libopenjp2-7 libpaper-utils libpaper1 libpng16-16 libssl1.1 libtiff5
  libwebp6 libwebpmux3 libx11-6 libx11-data libxau6 libxcb1 libxdmcp6 libxext6 libxml2 neofetch poppler-data
  shared-mime-info tzdata ucf xdg-user-dirs
0 upgraded, 66 newly installed, 0 to remove and 4 not upgraded.
Need to get 36.2 MB of archives.
After this operation, 136 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu focal/main amd64 fonts-droid-fallback all 1:6.0.1r16-1.1 [1805 kB]
Get:2 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libgomp1 amd64 10.3.0-1ubuntu1~20.04 [102 kB]
Get:3 http://archive.ubuntu.com/ubuntu focal/main amd64 libfftw3-double3 amd64 3.3.8-2ubuntu1 [728 kB]
Get:4 http://archive.ubuntu.com/ubuntu focal/main amd64 libexpat1 amd64 2.2.9-1build1 [73.3 kB]
Get:5 http://archive.ubuntu.com/ubuntu focal/main amd64 libpng16-16 amd64 1.6.37-2 [179 kB]
Get:6 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libfreetype6 amd64 2.10.1-2ubuntu0.1 [341 kB]
Get:7 http://archive.ubuntu.com/ubuntu focal/main amd64 ucf all 3.0038+nmu1 [51.6 kB]
Get:8 http://archive.ubuntu.com/ubuntu focal/main amd64 fonts-dejavu-core all 2.37-1 [1041 kB]
Get:9 http://archive.ubuntu.com/ubuntu focal/main amd64 fontconfig-config all 2.13.1-2ubuntu3 [28.8 kB]
Get:10 http://archive.ubuntu.com/ubuntu focal/main amd64 libfontconfig1 amd64 2.13.1-2ubuntu3 [114 kB]
Get:11 http://archive.ubuntu.com/ubuntu focal/main amd64 libjbig0 amd64 2.1-3.1build1 [26.7 kB]
Get:12 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libjpeg-turbo8 amd64 2.0.3-0ubuntu1.20.04.1 [117 kB]
Get:13 http://archive.ubuntu.com/ubuntu focal/main amd64 libjpeg8 amd64 8c-2ubuntu8 [2194 B]
Get:14 http://archive.ubuntu.com/ubuntu focal/main amd64 liblcms2-2 amd64 2.9-4 [140 kB]
Get:15 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libglib2.0-0 amd64 2.64.6-1~ubuntu20.04.4 [1287 kB]
Get:16 http://archive.ubuntu.com/ubuntu focal/universe amd64 liblqr-1-0 amd64 0.4.2-2.1 [27.7 kB]
Get:17 http://archive.ubuntu.com/ubuntu focal/main amd64 libltdl7 amd64 2.4.6-14 [38.5 kB]
Get:18 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libwebp6 amd64 0.6.1-2ubuntu0.20.04.1 [185 kB]
Get:19 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libtiff5 amd64 4.1.0+git191117-2ubuntu0.20.04.1 [162 kB]
Get:20 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libwebpmux3 amd64 0.6.1-2ubuntu0.20.04.1 [19.5 kB]
Get:21 http://archive.ubuntu.com/ubuntu focal/main amd64 libxau6 amd64 1:1.0.9-0ubuntu1 [7488 B]
Get:22 http://archive.ubuntu.com/ubuntu focal/main amd64 libbsd0 amd64 0.10.0-1 [45.4 kB]
Get:23 http://archive.ubuntu.com/ubuntu focal/main amd64 libxdmcp6 amd64 1:1.1.3-0ubuntu1 [10.6 kB]
Get:24 http://archive.ubuntu.com/ubuntu focal/main amd64 libxcb1 amd64 1.14-2 [44.7 kB]
Get:25 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libx11-data all 2:1.6.9-2ubuntu1.2 [113 kB]
Get:26 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libx11-6 amd64 2:1.6.9-2ubuntu1.2 [575 kB]
Get:27 http://archive.ubuntu.com/ubuntu focal/main amd64 libxext6 amd64 2:1.3.4-0ubuntu1 [29.1 kB]
Get:28 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 tzdata all 2021a-0ubuntu0.20.04 [295 kB]
Get:29 http://archive.ubuntu.com/ubuntu focal/main amd64 libicu66 amd64 66.1-2ubuntu2 [8520 kB]
Get:30 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libxml2 amd64 2.9.10+dfsg-5ubuntu0.20.04.1 [640 kB]
Get:31 http://archive.ubuntu.com/ubuntu focal-updates/universe amd64 imagemagick-6-common all 8:6.9.10.23+dfsg-2.1ubuntu11.4 [60.9 kB]
Get:32 http://archive.ubuntu.com/ubuntu focal-updates/universe amd64 libmagickcore-6.q16-6 amd64 8:6.9.10.23+dfsg-2.1ubuntu11.4 [1647 kB]
Get:33 http://archive.ubuntu.com/ubuntu focal-updates/universe amd64 libmagickwand-6.q16-6 amd64 8:6.9.10.23+dfsg-2.1ubuntu11.4 [303 kB]
Get:34 http://archive.ubuntu.com/ubuntu focal/main amd64 poppler-data all 0.4.9-2 [1475 kB]
Get:35 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libapparmor1 amd64 2.13.3-7ubuntu5.1 [34.1 kB]
Get:36 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libdbus-1-3 amd64 1.12.16-2ubuntu2.1 [179 kB]
Get:37 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 dbus amd64 1.12.16-2ubuntu2.1 [151 kB]
Get:38 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libglib2.0-data all 2.64.6-1~ubuntu20.04.4 [6052 B]
Get:39 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libssl1.1 amd64 1.1.1f-1ubuntu2.5 [1320 kB]
Get:40 http://archive.ubuntu.com/ubuntu focal/main amd64 shared-mime-info amd64 1.15-1 [430 kB]
Get:41 http://archive.ubuntu.com/ubuntu focal/main amd64 xdg-user-dirs amd64 0.17-2ubuntu1 [48.3 kB]
Get:42 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 krb5-locales all 1.17-6ubuntu4.1 [11.4 kB]
Get:43 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libkrb5support0 amd64 1.17-6ubuntu4.1 [30.9 kB]
Get:44 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libk5crypto3 amd64 1.17-6ubuntu4.1 [79.9 kB]
Get:45 http://archive.ubuntu.com/ubuntu focal/main amd64 libkeyutils1 amd64 1.6-6ubuntu1 [10.2 kB]
Get:46 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libkrb5-3 amd64 1.17-6ubuntu4.1 [330 kB]
Get:47 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libgssapi-krb5-2 amd64 1.17-6ubuntu4.1 [121 kB]
Get:48 http://archive.ubuntu.com/ubuntu focal/universe amd64 libchafa0 amd64 1.2.1-1 [42.1 kB]
Get:49 http://archive.ubuntu.com/ubuntu focal/universe amd64 chafa amd64 1.2.1-1 [29.7 kB]
Get:50 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 fonts-noto-mono all 20200323-1build1~ubuntu20.04.1 [80.6 kB]
Get:51 http://archive.ubuntu.com/ubuntu focal/main amd64 fonts-urw-base35 all 20170801.1-3 [6333 kB]
Get:52 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libgs9-common all 9.50~dfsg-5ubuntu4.2 [681 kB]
Get:53 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libavahi-common-data amd64 0.7-4ubuntu7.1 [21.4 kB]
Get:54 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libavahi-common3 amd64 0.7-4ubuntu7.1 [21.7 kB]
Get:55 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libavahi-client3 amd64 0.7-4ubuntu7.1 [25.5 kB]
Get:56 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libcups2 amd64 2.3.1-9ubuntu1.1 [233 kB]
Get:57 http://archive.ubuntu.com/ubuntu focal/main amd64 libidn11 amd64 1.33-2.2ubuntu2 [46.2 kB]
Get:58 http://archive.ubuntu.com/ubuntu focal/main amd64 libijs-0.35 amd64 0.35-15 [15.7 kB]
Get:59 http://archive.ubuntu.com/ubuntu focal/main amd64 libjbig2dec0 amd64 0.18-1ubuntu1 [60.0 kB]
Get:60 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libopenjp2-7 amd64 2.3.1-1ubuntu4.20.04.1 [141 kB]
Get:61 http://archive.ubuntu.com/ubuntu focal/main amd64 libpaper1 amd64 1.1.28 [13.0 kB]
Get:62 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libgs9 amd64 9.50~dfsg-5ubuntu4.2 [2172 kB]
Get:63 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 ghostscript amd64 9.50~dfsg-5ubuntu4.2 [51.6 kB]
Get:64 http://archive.ubuntu.com/ubuntu focal/universe amd64 gsfonts all 1:8.11+urwcyr1.0.7~pre44-4.4 [3120 kB]
Get:65 http://archive.ubuntu.com/ubuntu focal/main amd64 libpaper-utils amd64 1.1.28 [8400 B]
Get:66 http://archive.ubuntu.com/ubuntu focal/universe amd64 neofetch all 7.0.0-1 [77.5 kB]
Fetched 36.2 MB in 2s (16.6 MB/s)     
debconf: delaying package configuration, since apt-utils is not installed
Selecting previously unselected package fonts-droid-fallback.
(Reading database ... 4127 files and directories currently installed.)
Preparing to unpack .../00-fonts-droid-fallback_1%3a6.0.1r16-1.1_all.deb ...
Unpacking fonts-droid-fallback (1:6.0.1r16-1.1) ...
Selecting previously unselected package libgomp1:amd64.
Preparing to unpack .../01-libgomp1_10.3.0-1ubuntu1~20.04_amd64.deb ...
Unpacking libgomp1:amd64 (10.3.0-1ubuntu1~20.04) ...
Selecting previously unselected package libfftw3-double3:amd64.
Preparing to unpack .../02-libfftw3-double3_3.3.8-2ubuntu1_amd64.deb ...
Unpacking libfftw3-double3:amd64 (3.3.8-2ubuntu1) ...
Selecting previously unselected package libexpat1:amd64.
Preparing to unpack .../03-libexpat1_2.2.9-1build1_amd64.deb ...
Unpacking libexpat1:amd64 (2.2.9-1build1) ...
Selecting previously unselected package libpng16-16:amd64.
Preparing to unpack .../04-libpng16-16_1.6.37-2_amd64.deb ...
Unpacking libpng16-16:amd64 (1.6.37-2) ...
Selecting previously unselected package libfreetype6:amd64.
Preparing to unpack .../05-libfreetype6_2.10.1-2ubuntu0.1_amd64.deb ...
Unpacking libfreetype6:amd64 (2.10.1-2ubuntu0.1) ...
Selecting previously unselected package ucf.
Preparing to unpack .../06-ucf_3.0038+nmu1_all.deb ...
Moving old data out of the way
Unpacking ucf (3.0038+nmu1) ...
Selecting previously unselected package fonts-dejavu-core.
Preparing to unpack .../07-fonts-dejavu-core_2.37-1_all.deb ...
Unpacking fonts-dejavu-core (2.37-1) ...
Selecting previously unselected package fontconfig-config.
Preparing to unpack .../08-fontconfig-config_2.13.1-2ubuntu3_all.deb ...
Unpacking fontconfig-config (2.13.1-2ubuntu3) ...
Selecting previously unselected package libfontconfig1:amd64.
Preparing to unpack .../09-libfontconfig1_2.13.1-2ubuntu3_amd64.deb ...
Unpacking libfontconfig1:amd64 (2.13.1-2ubuntu3) ...
Selecting previously unselected package libjbig0:amd64.
Preparing to unpack .../10-libjbig0_2.1-3.1build1_amd64.deb ...
Unpacking libjbig0:amd64 (2.1-3.1build1) ...
Selecting previously unselected package libjpeg-turbo8:amd64.
Preparing to unpack .../11-libjpeg-turbo8_2.0.3-0ubuntu1.20.04.1_amd64.deb ...
Unpacking libjpeg-turbo8:amd64 (2.0.3-0ubuntu1.20.04.1) ...
Selecting previously unselected package libjpeg8:amd64.
Preparing to unpack .../12-libjpeg8_8c-2ubuntu8_amd64.deb ...
Unpacking libjpeg8:amd64 (8c-2ubuntu8) ...
Selecting previously unselected package liblcms2-2:amd64.
Preparing to unpack .../13-liblcms2-2_2.9-4_amd64.deb ...
Unpacking liblcms2-2:amd64 (2.9-4) ...
Selecting previously unselected package libglib2.0-0:amd64.
Preparing to unpack .../14-libglib2.0-0_2.64.6-1~ubuntu20.04.4_amd64.deb ...
Unpacking libglib2.0-0:amd64 (2.64.6-1~ubuntu20.04.4) ...
Selecting previously unselected package liblqr-1-0:amd64.
Preparing to unpack .../15-liblqr-1-0_0.4.2-2.1_amd64.deb ...
Unpacking liblqr-1-0:amd64 (0.4.2-2.1) ...
Selecting previously unselected package libltdl7:amd64.
Preparing to unpack .../16-libltdl7_2.4.6-14_amd64.deb ...
Unpacking libltdl7:amd64 (2.4.6-14) ...
Selecting previously unselected package libwebp6:amd64.
Preparing to unpack .../17-libwebp6_0.6.1-2ubuntu0.20.04.1_amd64.deb ...
Unpacking libwebp6:amd64 (0.6.1-2ubuntu0.20.04.1) ...
Selecting previously unselected package libtiff5:amd64.
Preparing to unpack .../18-libtiff5_4.1.0+git191117-2ubuntu0.20.04.1_amd64.deb ...
Unpacking libtiff5:amd64 (4.1.0+git191117-2ubuntu0.20.04.1) ...
Selecting previously unselected package libwebpmux3:amd64.
Preparing to unpack .../19-libwebpmux3_0.6.1-2ubuntu0.20.04.1_amd64.deb ...
Unpacking libwebpmux3:amd64 (0.6.1-2ubuntu0.20.04.1) ...
Selecting previously unselected package libxau6:amd64.
Preparing to unpack .../20-libxau6_1%3a1.0.9-0ubuntu1_amd64.deb ...
Unpacking libxau6:amd64 (1:1.0.9-0ubuntu1) ...
Selecting previously unselected package libbsd0:amd64.
Preparing to unpack .../21-libbsd0_0.10.0-1_amd64.deb ...
Unpacking libbsd0:amd64 (0.10.0-1) ...
Selecting previously unselected package libxdmcp6:amd64.
Preparing to unpack .../22-libxdmcp6_1%3a1.1.3-0ubuntu1_amd64.deb ...
Unpacking libxdmcp6:amd64 (1:1.1.3-0ubuntu1) ...
Selecting previously unselected package libxcb1:amd64.
Preparing to unpack .../23-libxcb1_1.14-2_amd64.deb ...
Unpacking libxcb1:amd64 (1.14-2) ...
Selecting previously unselected package libx11-data.
Preparing to unpack .../24-libx11-data_2%3a1.6.9-2ubuntu1.2_all.deb ...
Unpacking libx11-data (2:1.6.9-2ubuntu1.2) ...
Selecting previously unselected package libx11-6:amd64.
Preparing to unpack .../25-libx11-6_2%3a1.6.9-2ubuntu1.2_amd64.deb ...
Unpacking libx11-6:amd64 (2:1.6.9-2ubuntu1.2) ...
Selecting previously unselected package libxext6:amd64.
Preparing to unpack .../26-libxext6_2%3a1.3.4-0ubuntu1_amd64.deb ...
Unpacking libxext6:amd64 (2:1.3.4-0ubuntu1) ...
Selecting previously unselected package tzdata.
Preparing to unpack .../27-tzdata_2021a-0ubuntu0.20.04_all.deb ...
Unpacking tzdata (2021a-0ubuntu0.20.04) ...
Selecting previously unselected package libicu66:amd64.
Preparing to unpack .../28-libicu66_66.1-2ubuntu2_amd64.deb ...
Unpacking libicu66:amd64 (66.1-2ubuntu2) ...
Selecting previously unselected package libxml2:amd64.
Preparing to unpack .../29-libxml2_2.9.10+dfsg-5ubuntu0.20.04.1_amd64.deb ...
Unpacking libxml2:amd64 (2.9.10+dfsg-5ubuntu0.20.04.1) ...
Selecting previously unselected package imagemagick-6-common.
Preparing to unpack .../30-imagemagick-6-common_8%3a6.9.10.23+dfsg-2.1ubuntu11.4_all.deb ...
Unpacking imagemagick-6-common (8:6.9.10.23+dfsg-2.1ubuntu11.4) ...
Selecting previously unselected package libmagickcore-6.q16-6:amd64.
Preparing to unpack .../31-libmagickcore-6.q16-6_8%3a6.9.10.23+dfsg-2.1ubuntu11.4_amd64.deb ...
Unpacking libmagickcore-6.q16-6:amd64 (8:6.9.10.23+dfsg-2.1ubuntu11.4) ...
Selecting previously unselected package libmagickwand-6.q16-6:amd64.
Preparing to unpack .../32-libmagickwand-6.q16-6_8%3a6.9.10.23+dfsg-2.1ubuntu11.4_amd64.deb ...
Unpacking libmagickwand-6.q16-6:amd64 (8:6.9.10.23+dfsg-2.1ubuntu11.4) ...
Selecting previously unselected package poppler-data.
Preparing to unpack .../33-poppler-data_0.4.9-2_all.deb ...
Unpacking poppler-data (0.4.9-2) ...
Selecting previously unselected package libapparmor1:amd64.
Preparing to unpack .../34-libapparmor1_2.13.3-7ubuntu5.1_amd64.deb ...
Unpacking libapparmor1:amd64 (2.13.3-7ubuntu5.1) ...
Selecting previously unselected package libdbus-1-3:amd64.
Preparing to unpack .../35-libdbus-1-3_1.12.16-2ubuntu2.1_amd64.deb ...
Unpacking libdbus-1-3:amd64 (1.12.16-2ubuntu2.1) ...
Selecting previously unselected package dbus.
Preparing to unpack .../36-dbus_1.12.16-2ubuntu2.1_amd64.deb ...
Unpacking dbus (1.12.16-2ubuntu2.1) ...
Selecting previously unselected package libglib2.0-data.
Preparing to unpack .../37-libglib2.0-data_2.64.6-1~ubuntu20.04.4_all.deb ...
Unpacking libglib2.0-data (2.64.6-1~ubuntu20.04.4) ...
Selecting previously unselected package libssl1.1:amd64.
Preparing to unpack .../38-libssl1.1_1.1.1f-1ubuntu2.5_amd64.deb ...
Unpacking libssl1.1:amd64 (1.1.1f-1ubuntu2.5) ...
Selecting previously unselected package shared-mime-info.
Preparing to unpack .../39-shared-mime-info_1.15-1_amd64.deb ...
Unpacking shared-mime-info (1.15-1) ...
Selecting previously unselected package xdg-user-dirs.
Preparing to unpack .../40-xdg-user-dirs_0.17-2ubuntu1_amd64.deb ...
Unpacking xdg-user-dirs (0.17-2ubuntu1) ...
Selecting previously unselected package krb5-locales.
Preparing to unpack .../41-krb5-locales_1.17-6ubuntu4.1_all.deb ...
Unpacking krb5-locales (1.17-6ubuntu4.1) ...
Selecting previously unselected package libkrb5support0:amd64.
Preparing to unpack .../42-libkrb5support0_1.17-6ubuntu4.1_amd64.deb ...
Unpacking libkrb5support0:amd64 (1.17-6ubuntu4.1) ...
Selecting previously unselected package libk5crypto3:amd64.
Preparing to unpack .../43-libk5crypto3_1.17-6ubuntu4.1_amd64.deb ...
Unpacking libk5crypto3:amd64 (1.17-6ubuntu4.1) ...
Selecting previously unselected package libkeyutils1:amd64.
Preparing to unpack .../44-libkeyutils1_1.6-6ubuntu1_amd64.deb ...
Unpacking libkeyutils1:amd64 (1.6-6ubuntu1) ...
Selecting previously unselected package libkrb5-3:amd64.
Preparing to unpack .../45-libkrb5-3_1.17-6ubuntu4.1_amd64.deb ...
Unpacking libkrb5-3:amd64 (1.17-6ubuntu4.1) ...
Selecting previously unselected package libgssapi-krb5-2:amd64.
Preparing to unpack .../46-libgssapi-krb5-2_1.17-6ubuntu4.1_amd64.deb ...
Unpacking libgssapi-krb5-2:amd64 (1.17-6ubuntu4.1) ...
Selecting previously unselected package libchafa0:amd64.
Preparing to unpack .../47-libchafa0_1.2.1-1_amd64.deb ...
Unpacking libchafa0:amd64 (1.2.1-1) ...
Selecting previously unselected package chafa.
Preparing to unpack .../48-chafa_1.2.1-1_amd64.deb ...
Unpacking chafa (1.2.1-1) ...
Selecting previously unselected package fonts-noto-mono.
Preparing to unpack .../49-fonts-noto-mono_20200323-1build1~ubuntu20.04.1_all.deb ...
Unpacking fonts-noto-mono (20200323-1build1~ubuntu20.04.1) ...
Selecting previously unselected package fonts-urw-base35.
Preparing to unpack .../50-fonts-urw-base35_20170801.1-3_all.deb ...
Unpacking fonts-urw-base35 (20170801.1-3) ...
Selecting previously unselected package libgs9-common.
Preparing to unpack .../51-libgs9-common_9.50~dfsg-5ubuntu4.2_all.deb ...
Unpacking libgs9-common (9.50~dfsg-5ubuntu4.2) ...
Selecting previously unselected package libavahi-common-data:amd64.
Preparing to unpack .../52-libavahi-common-data_0.7-4ubuntu7.1_amd64.deb ...
Unpacking libavahi-common-data:amd64 (0.7-4ubuntu7.1) ...
Selecting previously unselected package libavahi-common3:amd64.
Preparing to unpack .../53-libavahi-common3_0.7-4ubuntu7.1_amd64.deb ...
Unpacking libavahi-common3:amd64 (0.7-4ubuntu7.1) ...
Selecting previously unselected package libavahi-client3:amd64.
Preparing to unpack .../54-libavahi-client3_0.7-4ubuntu7.1_amd64.deb ...
Unpacking libavahi-client3:amd64 (0.7-4ubuntu7.1) ...
Selecting previously unselected package libcups2:amd64.
Preparing to unpack .../55-libcups2_2.3.1-9ubuntu1.1_amd64.deb ...
Unpacking libcups2:amd64 (2.3.1-9ubuntu1.1) ...
Selecting previously unselected package libidn11:amd64.
Preparing to unpack .../56-libidn11_1.33-2.2ubuntu2_amd64.deb ...
Unpacking libidn11:amd64 (1.33-2.2ubuntu2) ...
Selecting previously unselected package libijs-0.35:amd64.
Preparing to unpack .../57-libijs-0.35_0.35-15_amd64.deb ...
Unpacking libijs-0.35:amd64 (0.35-15) ...
Selecting previously unselected package libjbig2dec0:amd64.
Preparing to unpack .../58-libjbig2dec0_0.18-1ubuntu1_amd64.deb ...
Unpacking libjbig2dec0:amd64 (0.18-1ubuntu1) ...
Selecting previously unselected package libopenjp2-7:amd64.
Preparing to unpack .../59-libopenjp2-7_2.3.1-1ubuntu4.20.04.1_amd64.deb ...
Unpacking libopenjp2-7:amd64 (2.3.1-1ubuntu4.20.04.1) ...
Selecting previously unselected package libpaper1:amd64.
Preparing to unpack .../60-libpaper1_1.1.28_amd64.deb ...
Unpacking libpaper1:amd64 (1.1.28) ...
Selecting previously unselected package libgs9:amd64.
Preparing to unpack .../61-libgs9_9.50~dfsg-5ubuntu4.2_amd64.deb ...
Unpacking libgs9:amd64 (9.50~dfsg-5ubuntu4.2) ...
Selecting previously unselected package ghostscript.
Preparing to unpack .../62-ghostscript_9.50~dfsg-5ubuntu4.2_amd64.deb ...
Unpacking ghostscript (9.50~dfsg-5ubuntu4.2) ...
Selecting previously unselected package gsfonts.
Preparing to unpack .../63-gsfonts_1%3a8.11+urwcyr1.0.7~pre44-4.4_all.deb ...
Unpacking gsfonts (1:8.11+urwcyr1.0.7~pre44-4.4) ...
Selecting previously unselected package libpaper-utils.
Preparing to unpack .../64-libpaper-utils_1.1.28_amd64.deb ...
Unpacking libpaper-utils (1.1.28) ...
Selecting previously unselected package neofetch.
Preparing to unpack .../65-neofetch_7.0.0-1_all.deb ...
Unpacking neofetch (7.0.0-1) ...
Setting up libexpat1:amd64 (2.2.9-1build1) ...
Setting up liblcms2-2:amd64 (2.9-4) ...
Setting up libxau6:amd64 (1:1.0.9-0ubuntu1) ...
Setting up imagemagick-6-common (8:6.9.10.23+dfsg-2.1ubuntu11.4) ...
Setting up libkeyutils1:amd64 (1.6-6ubuntu1) ...
Setting up libapparmor1:amd64 (2.13.3-7ubuntu5.1) ...
Setting up fonts-noto-mono (20200323-1build1~ubuntu20.04.1) ...
Setting up xdg-user-dirs (0.17-2ubuntu1) ...
Setting up libglib2.0-0:amd64 (2.64.6-1~ubuntu20.04.4) ...
No schema files found: doing nothing.
Setting up libssl1.1:amd64 (1.1.1f-1ubuntu2.5) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be used. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 76.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC contains: /etc/perl /usr/local/lib/x86_64-linux-gnu/perl/5.30.0 /usr/local/share/perl/5.30.0 /usr/lib/x86_64-linux-gnu/perl5/5.30 /usr/share/perl5 /usr/lib/x86_64-linux-gnu/perl/5.30 /usr/share/perl/5.30 /usr/local/lib/site_perl /usr/lib/x86_64-linux-gnu/perl-base) at /usr/share/perl5/Debconf/FrontEnd/Readline.pm line 7.)
debconf: falling back to frontend: Teletype
Setting up libijs-0.35:amd64 (0.35-15) ...
Setting up krb5-locales (1.17-6ubuntu4.1) ...
Setting up fonts-urw-base35 (20170801.1-3) ...
Setting up libgomp1:amd64 (10.3.0-1ubuntu1~20.04) ...
Setting up libjbig0:amd64 (2.1-3.1build1) ...
Setting up neofetch (7.0.0-1) ...
Setting up poppler-data (0.4.9-2) ...
Setting up libkrb5support0:amd64 (1.17-6ubuntu4.1) ...
Setting up libchafa0:amd64 (1.2.1-1) ...
Setting up tzdata (2021a-0ubuntu0.20.04) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be used. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 76.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC contains: /etc/perl /usr/local/lib/x86_64-linux-gnu/perl/5.30.0 /usr/local/share/perl/5.30.0 /usr/lib/x86_64-linux-gnu/perl5/5.30 /usr/share/perl5 /usr/lib/x86_64-linux-gnu/perl/5.30 /usr/share/perl/5.30 /usr/local/lib/site_perl /usr/lib/x86_64-linux-gnu/perl-base) at /usr/share/perl5/Debconf/FrontEnd/Readline.pm line 7.)
debconf: falling back to frontend: Teletype
Configuring tzdata
------------------

Please select the geographic area in which you live. Subsequent configuration questions will narrow this down by
presenting a list of cities, representing the time zones in which they are located.

  1. Africa   3. Antarctica  5. Arctic  7. Atlantic  9. Indian    11. SystemV  13. Etc
  2. America  4. Australia   6. Asia    8. Europe    10. Pacific  12. US
Geographic area: 2

Please select the city or region corresponding to your time zone.

  1. Adak                     40. Costa_Rica            79. Juneau                   118. Port-au-Prince
  2. Anchorage                41. Creston               80. Kentucky/Louisville      119. Port_of_Spain
  3. Anguilla                 42. Cuiaba                81. Kentucky/Monticello      120. Porto_Acre
  4. Antigua                  43. Curacao               82. Kralendijk               121. Porto_Velho
  5. Araguaina                44. Danmarkshavn          83. La_Paz                   122. Puerto_Rico
  6. Argentina/Buenos_Aires   45. Dawson                84. Lima                     123. Punta_Arenas
  7. Argentina/Catamarca      46. Dawson_Creek          85. Los_Angeles              124. Rainy_River
  8. Argentina/Cordoba        47. Denver                86. Lower_Princes            125. Rankin_Inlet
  9. Argentina/Jujuy          48. Detroit               87. Maceio                   126. Recife
  10. Argentina/La_Rioja      49. Dominica              88. Managua                  127. Regina
  11. Argentina/Mendoza       50. Edmonton              89. Manaus                   128. Resolute
  12. Argentina/Rio_Gallegos  51. Eirunepe              90. Marigot                  129. Rio_Branco
  13. Argentina/Salta         52. El_Salvador           91. Martinique               130. Santa_Isabel
  14. Argentina/San_Juan      53. Ensenada              92. Matamoros                131. Santarem
  15. Argentina/San_Luis      54. Fort_Nelson           93. Mazatlan                 132. Santiago
  16. Argentina/Tucuman       55. Fortaleza             94. Menominee                133. Santo_Domingo
  17. Argentina/Ushuaia       56. Glace_Bay             95. Merida                   134. Sao_Paulo
  18. Aruba                   57. Godthab               96. Metlakatla               135. Scoresbysund
  19. Asuncion                58. Goose_Bay             97. Mexico_City              136. Shiprock
  20. Atikokan                59. Grand_Turk            98. Miquelon                 137. Sitka
[More] 126

  21. Atka                    60. Grenada               99. Moncton                  138. St_Barthelemy
  22. Bahia                   61. Guadeloupe            100. Monterrey               139. St_Johns
  23. Bahia_Banderas          62. Guatemala             101. Montevideo              140. St_Kitts
  24. Barbados                63. Guayaquil             102. Montreal                141. St_Lucia
  25. Belem                   64. Guyana                103. Montserrat              142. St_Thomas
  26. Belize                  65. Halifax               104. Nassau                  143. St_Vincent
  27. Blanc-Sablon            66. Havana                105. New_York                144. Swift_Current
  28. Boa_Vista               67. Hermosillo            106. Nipigon                 145. Tegucigalpa
  29. Bogota                  68. Indiana/Indianapolis  107. Nome                    146. Thule
  30. Boise                   69. Indiana/Knox          108. Noronha                 147. Thunder_Bay
  31. Cambridge_Bay           70. Indiana/Marengo       109. North_Dakota/Beulah     148. Tijuana
  32. Campo_Grande            71. Indiana/Petersburg    110. North_Dakota/Center     149. Toronto
  33. Cancun                  72. Indiana/Tell_City     111. North_Dakota/New_Salem  150. Tortola
  34. Caracas                 73. Indiana/Vevay         112. Nuuk                    151. Vancouver
  35. Cayenne                 74. Indiana/Vincennes     113. Ojinaga                 152. Virgin
  36. Cayman                  75. Indiana/Winamac       114. Panama                  153. Whitehorse
  37. Chicago                 76. Inuvik                115. Pangnirtung             154. Winnipeg
  38. Chihuahua               77. Iqaluit               116. Paramaribo              155. Yakutat
  39. Coral_Harbour           78. Jamaica               117. Phoenix                 156. Yellowknife
Time zone: 

Time zone: 126


Current default time zone: 'America/Recife'
Local time is now:      Tue Aug 24 02:57:35 -03 2021.
Universal Time is now:  Tue Aug 24 05:57:35 UTC 2021.
Run 'dpkg-reconfigure tzdata' if you wish to change it.

Setting up libglib2.0-data (2.64.6-1~ubuntu20.04.4) ...
Setting up libx11-data (2:1.6.9-2ubuntu1.2) ...
Setting up libjbig2dec0:amd64 (0.18-1ubuntu1) ...
Setting up libidn11:amd64 (1.33-2.2ubuntu2) ...
Setting up gsfonts (1:8.11+urwcyr1.0.7~pre44-4.4) ...
Setting up libavahi-common-data:amd64 (0.7-4ubuntu7.1) ...
Setting up libdbus-1-3:amd64 (1.12.16-2ubuntu2.1) ...
Setting up dbus (1.12.16-2ubuntu2.1) ...
Setting up libpng16-16:amd64 (1.6.37-2) ...
Setting up libwebp6:amd64 (0.6.1-2ubuntu0.20.04.1) ...
Setting up fonts-dejavu-core (2.37-1) ...
Setting up ucf (3.0038+nmu1) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be used. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 76.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC contains: /etc/perl /usr/local/lib/x86_64-linux-gnu/perl/5.30.0 /usr/local/share/perl/5.30.0 /usr/lib/x86_64-linux-gnu/perl5/5.30 /usr/share/perl5 /usr/lib/x86_64-linux-gnu/perl/5.30 /usr/share/perl/5.30 /usr/local/lib/site_perl /usr/lib/x86_64-linux-gnu/perl-base) at /usr/share/perl5/Debconf/FrontEnd/Readline.pm line 7.)
debconf: falling back to frontend: Teletype
Setting up libk5crypto3:amd64 (1.17-6ubuntu4.1) ...
Setting up libjpeg-turbo8:amd64 (2.0.3-0ubuntu1.20.04.1) ...
Setting up libltdl7:amd64 (2.4.6-14) ...
Setting up libfftw3-double3:amd64 (3.3.8-2ubuntu1) ...
Setting up liblqr-1-0:amd64 (0.4.2-2.1) ...
Setting up libopenjp2-7:amd64 (2.3.1-1ubuntu4.20.04.1) ...
Setting up libkrb5-3:amd64 (1.17-6ubuntu4.1) ...
Setting up fonts-droid-fallback (1:6.0.1r16-1.1) ...
Setting up libwebpmux3:amd64 (0.6.1-2ubuntu0.20.04.1) ...
Setting up libbsd0:amd64 (0.10.0-1) ...
Setting up libjpeg8:amd64 (8c-2ubuntu8) ...
Setting up libgs9-common (9.50~dfsg-5ubuntu4.2) ...
Setting up libpaper1:amd64 (1.1.28) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be used. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 76.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC contains: /etc/perl /usr/local/lib/x86_64-linux-gnu/perl/5.30.0 /usr/local/share/perl/5.30.0 /usr/lib/x86_64-linux-gnu/perl5/5.30 /usr/share/perl5 /usr/lib/x86_64-linux-gnu/perl/5.30 /usr/share/perl/5.30 /usr/local/lib/site_perl /usr/lib/x86_64-linux-gnu/perl-base) at /usr/share/perl5/Debconf/FrontEnd/Readline.pm line 7.)
debconf: falling back to frontend: Teletype

Creating config file /etc/papersize with new version
Setting up libxdmcp6:amd64 (1:1.1.3-0ubuntu1) ...
Setting up libxcb1:amd64 (1.14-2) ...
Setting up fontconfig-config (2.13.1-2ubuntu3) ...
Setting up libicu66:amd64 (66.1-2ubuntu2) ...
Setting up libavahi-common3:amd64 (0.7-4ubuntu7.1) ...
Setting up libpaper-utils (1.1.28) ...
Setting up libfreetype6:amd64 (2.10.1-2ubuntu0.1) ...
Setting up libgssapi-krb5-2:amd64 (1.17-6ubuntu4.1) ...
Setting up libx11-6:amd64 (2:1.6.9-2ubuntu1.2) ...
Setting up libtiff5:amd64 (4.1.0+git191117-2ubuntu0.20.04.1) ...
Setting up libfontconfig1:amd64 (2.13.1-2ubuntu3) ...
Setting up libxml2:amd64 (2.9.10+dfsg-5ubuntu0.20.04.1) ...
Setting up libavahi-client3:amd64 (0.7-4ubuntu7.1) ...
Setting up libxext6:amd64 (2:1.3.4-0ubuntu1) ...
Setting up libmagickcore-6.q16-6:amd64 (8:6.9.10.23+dfsg-2.1ubuntu11.4) ...
Setting up shared-mime-info (1.15-1) ...
Setting up libcups2:amd64 (2.3.1-9ubuntu1.1) ...
Setting up libmagickwand-6.q16-6:amd64 (8:6.9.10.23+dfsg-2.1ubuntu11.4) ...
Setting up libgs9:amd64 (9.50~dfsg-5ubuntu4.2) ...
Setting up chafa (1.2.1-1) ...
Setting up ghostscript (9.50~dfsg-5ubuntu4.2) ...
Processing triggers for libc-bin (2.31-0ubuntu9.2) ...
root@675d5758f359:/# neofetch 
            .-/+oossssoo+/-.               root@675d5758f359 
        `:+ssssssssssssssssss+:`           ----------------- 
      -+ssssssssssssssssssyyssss+-         OS: Ubuntu 20.04.2 LTS focal x86_64 
    .ossssssssssssssssssdMMMNysssso.       Host: Virtual Machine 7.0 
   /ssssssssssshdmmNNmmyNMMMMhssssss/      Kernel: 4.4.0-210-generic 
  +ssssssssshmydMMMMMMMNddddyssssssss+     Uptime: 46 days, 17 hours, 59 mins 
 /sssssssshNMMMyhhyyyyhmNMMMNhssssssss/    Packages: 158 (dpkg) 
.ssssssssdMMMNhsssssssssshNMMMdssssssss.   Shell: bash 5.0.17 
+sssshhhyNMMNyssssssssssssyNMMMysssssss+   CPU: Intel Xeon E5-2673 v4 (8) @ 2.294GHz 
ossyNMMMNyMMhsssssssssssssshmmmhssssssso   Memory: 17251MiB / 32174MiB 
ossyNMMMNyMMhsssssssssssssshmmmhssssssso
+sssshhhyNMMNyssssssssssssyNMMMysssssss+                           
.ssssssssdMMMNhsssssssssshNMMMdssssssss.                           
 /sssssssshNMMMyhhyyyyhdNMMMNhssssssss/
  +sssssssssdmydMMMMMMMMddddyssssssss+
   /ssssssssssshdmNNNNmyNMMMMhssssss/
    .ossssssssssssssssssdMMMNysssso.
      -+sssssssssssssssssyyyssss+-
        `:+ssssssssssssssssss+:`
            .-/+oossssoo+/-.

root@675d5758f359:/# vi
vigr  vipw  
root@675d5758f359:/# na
namei  nawk   
root@675d5758f359:/# ^C
root@675d5758f359:/# exit
[node1] (local) root@192.168.0.8 ~
$ docker run --name ubuntinho -it ubuntu bash
docker: Error response from daemon: Conflict. The container name "/ubuntinho" is already in use by container "675d5758f3592bdcc258222e8b5543976013d2a8f17b0e4f64b83ff2f625429b". You have to remove (or rename) that container to be able to reuse that name.
See 'docker run --help'.
[node1] (local) root@192.168.0.8 ~
$ history 
    1  ls
    2  git clone htts://github.com/luistkd4/docker101
    3  git clone https://github.com/luistkd4/docker101
    4  ls
    5  cd docker101/
    6  cd IntroComands/
    7  ls
    8  vim principais_comandos.sh 
    9  cat I
   10  cat principais_comandos.sh 
   11  wget https://github.com/wagoodman/dive/releases/download/v0.9.2/dive_0.9.2_linux_amd64.deb
   12  sudo apt install ./dive_0.9.2_linux_amd64.deb
   13  cd
   14  sudo su 
   15  docker run --name newcontainer hello-world
   16  docker run --name hello -d buybox sleep 3600
   17  docker run --name hello -d busybox sleep 3600
   18  docker ps
   19  docker run --name site -d -p 80:80 nginx
   20  docker ps
   21  curl nginix
   22  curl nginx
   23  curl localhost
   24  netstat -nltp
   25  man curl
   26* 
   27  docker ps
   28  docker ls
   29  docker -a
   30  docker ps
   31  docker ps -a
   32  docker ps
   33  docker exec hello mkdir teste
   34  docker exec -it hello sh 
   35  docker stop site
   36  docker ps
   37  curl localhost
   38  netstat -nltp
   39  docker start site
   40  curl localhost
   41  netstat -nltp
   42  docker logs site
   43  docker logs site
   44  docker image
   45  docker images
   46  docker run debian
   47  docker images
   48  history 
   49  docker run --name debian debian
   50  docker images
   51  docker start debian
   52  docker start debian -it bash
   53  docker ps -a
   54  docker start 8464caa2b67c  -it bash
   55  docker images
   56  docker run debian
   57  docker status debian
   58  docker stats debian
   59  docker exec debian
   60  docker exec debian -it bash
   61  docker exec debian -it
   62  docker exec debian -it -d debian 
   63  docker exec debian -it -d debian /bin/bash
   64  docker run -it -d ubuntu /bin/bash
   65  docker ps
   66  docker start ubuntu 
   67  docker start 5a004080b69a
   68  docker ps
   69  docker run ubuntu
   70  docker run ubuntu -it ubuntu bash
   71  docker run ubuntu:latest 
   72  docker run ubuntu -it ubuntu bash
   73  docker run --name ubuntinho -it ubuntu bash
   74  docker run --name ubuntinho -it ubuntu bash
   75  history 
[node1] (local) root@192.168.0.8 ~
$ 
[node1] (local) root@192.168.0.8 ~
$ 
[node1] (local) root@192.168.0.8 ~
$ git clone https://github.com/alexsandro-matias/comandos-basicos-docker.git
Cloning into 'comandos-basicos-docker'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
[node1] (local) root@192.168.0.8 ~
$ ls
comandos-basicos-docker  docker101
[node1] (local) root@192.168.0.8 ~
$ cd comandos-basicos-docker/
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ history 
    1  ls
    2  git clone htts://github.com/luistkd4/docker101
    3  git clone https://github.com/luistkd4/docker101
    4  ls
    5  cd docker101/
    6  cd IntroComands/
    7  ls
    8  vim principais_comandos.sh 
    9  cat I
   10  cat principais_comandos.sh 
   11  wget https://github.com/wagoodman/dive/releases/download/v0.9.2/dive_0.9.2_linux_amd64.deb
   12  sudo apt install ./dive_0.9.2_linux_amd64.deb
   13  cd
   14  sudo su 
   15  docker run --name newcontainer hello-world
   16  docker run --name hello -d buybox sleep 3600
   17  docker run --name hello -d busybox sleep 3600
   18  docker ps
   19  docker run --name site -d -p 80:80 nginx
   20  docker ps
   21  curl nginix
   22  curl nginx
   23  curl localhost
   24  netstat -nltp
   25  man curl
   26* 
   27  docker ps
   28  docker ls
   29  docker -a
   30  docker ps
   31  docker ps -a
   32  docker ps
   33  docker exec hello mkdir teste
   34  docker exec -it hello sh 
   35  docker stop site
   36  docker ps
   37  curl localhost
   38  netstat -nltp
   39  docker start site
   40  curl localhost
   41  netstat -nltp
   42  docker logs site
   43  docker logs site
   44  docker image
   45  docker images
   46  docker run debian
   47  docker images
   48  history 
   49  docker run --name debian debian
   50  docker images
   51  docker start debian
   52  docker start debian -it bash
   53  docker ps -a
   54  docker start 8464caa2b67c  -it bash
   55  docker images
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ history >> .
bash: .: Is a directory
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ history >> 
bash: syntax error near unexpected token `newline'
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ history >> comandos docker.md
bash: history: docker.md: numeric argument required
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ history > comandos docker.md
bash: history: docker.md: numeric argument required
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ history >> docker.md
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ ls
README.md  comandos   docker.md
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ cat comandos 
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ cat docker.md 
    1  ls
    2  git clone htts://github.com/luistkd4/docker101
    3  git clone https://github.com/luistkd4/docker101
    4  ls
    5  cd docker101/
    6  cd IntroComands/
    7  ls
    8  vim principais_comandos.sh 
    9  cat I
   10  cat principais_comandos.sh 
   11  wget https://github.com/wagoodman/dive/releases/download/v0.9.2/dive_0.9.2_linux_amd64.deb
   12  sudo apt install ./dive_0.9.2_linux_amd64.deb
   13  cd
   14  sudo su 
   15  docker run --name newcontainer hello-world
   16  docker run --name hello -d buybox sleep 3600
   17  docker run --name hello -d busybox sleep 3600
   18  docker ps
   19  docker run --name site -d -p 80:80 nginx
   20  docker ps
   21  curl nginix
   22  curl nginx
   23  curl localhost
   24  netstat -nltp
   25  man curl
   26* 
   27  docker ps
   28  docker ls
   29  docker -a
   30  docker ps
   31  docker ps -a
   32  docker ps
   33  docker exec hello mkdir teste
   34  docker exec -it hello sh 
   35  docker stop site
   36  docker ps
   37  curl localhost
   38  netstat -nltp
   39  docker start site
   40  curl localhost
   41  netstat -nltp
   42  docker logs site
   43  docker logs site
   44  docker image
   45  docker images
   46  docker run debian
   47  docker images
   48  history 
   49  docker run --name debian debian
   50  docker images
   51  docker start debian
   52  docker start debian -it bash
   53  docker ps -a
   54  docker start 8464caa2b67c  -it bash
   55  docker images
   56  docker run debian
   57  docker status debian
   58  docker stats debian
   59  docker exec debian
   60  docker exec debian -it bash
   61  docker exec debian -it
   62  docker exec debian -it -d debian 
   63  docker exec debian -it -d debian /bin/bash
   64  docker run -it -d ubuntu /bin/bash
   65  docker ps
   66  docker start ubuntu 
   67  docker start 5a004080b69a
   68  docker ps
   69  docker run ubuntu
   70  docker run ubuntu -it ubuntu bash
   71  docker run ubuntu:latest 
   72  docker run ubuntu -it ubuntu bash
   73  docker run --name ubuntinho -it ubuntu bash
   74  docker run --name ubuntinho -it ubuntu bash
   75  history 
   76  git clone https://github.com/alexsandro-matias/comandos-basicos-docker.git
   77  ls
   78  cd comandos-basicos-docker/
   79  history 
   80  history >> .
   81  history >> 
   82  history >> comandos docker.md
   83  history > comandos docker.md
   84  history >> docker.md
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ git add .
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ git commit -m "primeiros comandos"

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'root@node1.(none)')
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ git config --global user.email "matiasalexsandro@gmail.com"
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ git config --global user.name "alexsandro-matias"
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ git add .
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ git commit -m "primeiros comandos"
[main be005ea] primeiros comandos
 2 files changed, 84 insertions(+)
 create mode 100644 comandos
 create mode 100644 docker.md
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ git push 
Username for 'https://github.com': alexsandro-matias
Password for 'https://alexsandro-matias@github.com': 
remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
fatal: Authentication failed for 'https://github.com/alexsandro-matias/comandos-basicos-docker.git/'
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ git push 
Username for 'https://github.com': alexsandro-matias
Password for 'https://alexsandro-matias@github.com': 
remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
fatal: Authentication failed for 'https://github.com/alexsandro-matias/comandos-basicos-docker.git/'
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ pwd
/root/comandos-basicos-docker
[node1] (local) root@192.168.0.8 ~/comandos-basicos-docker
$ cd ..
[node1] (local) root@192.168.0.8 ~
$ rm -f 
.cache/                  .inputrc                 .viminfo                 docker101/
.docker/                 .profile                 .vimrc                   
.gitconfig               .ssh/                    comandos-basicos-docker/ 
[node1] (local) root@192.168.0.8 ~
$ rm -f comandos-basicos-docker/
rm: 'comandos-basicos-docker' is a directory
[node1] (local) root@192.168.0.8 ~
$ rmdir -f comandos-basicos-docker/
rmdir: unrecognized option: f
BusyBox v1.31.1 () multi-call binary.

Usage: rmdir [OPTIONS] DIRECTORY...

Remove DIRECTORY if it is empty

        -p      Include parents
        --ignore-fail-on-non-empty
[node1] (local) root@192.168.0.8 ~
$ rm -Rf comandos-basicos-docker/
[node1] (local) root@192.168.0.8 ~
$ ls
docker101
[node1] (local) root@192.168.0.8 ~
$ git clone https://github.com/alexsandro-matias/comandos-basicos-docker.git
Cloning into 'comandos-basicos-docker'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
[node1] (local) root@192.168.0.8 ~
$ rm -Rf comandos-basicos-docker/
[node1] (local) root@192.168.0.8 ~
$ git@github.com:alexsandro-matias/comandos-basicos-docker.git
bash: git@github.com:alexsandro-matias/comandos-basicos-docker.git: No such file or directory
[node1] (local) root@192.168.0.8 ~
$ ssh -v
usage: ssh [-46AaCfGgKkMNnqsTtVvXxYy] [-B bind_interface]
           [-b bind_address] [-c cipher_spec] [-D [bind_address:]port]
           [-E log_file] [-e escape_char] [-F configfile] [-I pkcs11]
           [-i identity_file] [-J [user@]host[:port]] [-L address]
           [-l login_name] [-m mac_spec] [-O ctl_cmd] [-o option] [-p port]
           [-Q query_option] [-R address] [-S ctl_path] [-W host:port]
           [-w local_tun[:remote_tun]] destination [command]
[node1] (local) root@192.168.0.8 ~
$ 
