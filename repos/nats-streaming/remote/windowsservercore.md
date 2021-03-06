## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:786a11faed09783fa9192def766e3faf0b8d9d7f84dae107dda1ed644db8dbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1884; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.14393.1884; amd64

```console
$ docker pull nats-streaming@sha256:92f09b587e69a4bd899cbb58d136cd72088719884734fa46c96429b290a3b69d
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5360147726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abe4f9a7dee5d03cb7065a7292508b3132f05eccc1f33ef39d3414432053c2b`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 13 Nov 2017 21:42:13 GMT
RUN Install update 10.0.14393.1884
# Tue, 14 Nov 2017 23:32:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Nov 2017 23:32:15 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Tue, 14 Nov 2017 23:32:17 GMT
RUN cmd /S /C #(nop) COPY file:c656ebbfbb58cb37d445aa025a3f93117bfda2b77866533dfe567a67a4a71e01 in nats-streaming-server.exe 
# Tue, 14 Nov 2017 23:32:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222/tcp 8222/tcp
# Tue, 14 Nov 2017 23:32:18 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 13 Dec 2016 10:53:31 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ead9f4ead3c5a712cb213a5318f4a8bf3604bc16e16ce4f7cf0b66f7d2073282`  
		Last Modified: Mon, 13 Nov 2017 21:42:13 GMT  
		Size: 1.3 GB (1286993027 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:139303713dae40ff590b66954070b5354fdf1da3648e90a3888b4c2e9a8a197a`  
		Last Modified: Tue, 14 Nov 2017 23:32:38 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac416d81cb7205cf76cec30a26efaa091b4a73e640f9a5665e4f9abf0528d48`  
		Last Modified: Tue, 14 Nov 2017 23:32:38 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb95c5c363b1a76a76f7324af8c93caf678d90fd884056d2c432d02422c29a99`  
		Last Modified: Tue, 14 Nov 2017 23:32:39 GMT  
		Size: 3.2 MB (3163879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e90c6562a903a315eaa50cb60b29cab41641d803f8bfbc1535133ad0abea86d`  
		Last Modified: Tue, 14 Nov 2017 23:32:38 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32e3abb9679b55c2d9a80fd8557754076047ad569abf0f323dea77a06cf7418`  
		Last Modified: Tue, 14 Nov 2017 23:32:38 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
