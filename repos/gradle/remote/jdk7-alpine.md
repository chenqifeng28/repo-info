## `gradle:jdk7-alpine`

```console
$ docker pull gradle@sha256:951050189d7f7730fd4a37f53aacf15ec534d41f8391d4a9d030dfbb4f7995e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gradle:jdk7-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:c83ab32d73a423c17fcefc914b5045d96302d8927a30fa37a27e61e716923d2a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152791080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c305b4051d1f372f469e0408556a73babf19dd18aaa2c1d6b71f5bd6685c05c`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Nov 2017 22:10:18 GMT
ADD file:1e87ff33d1b6765b793888cd50e01b2bd0dfe152b7dbb4048008bfc2658faea7 in / 
# Fri, 03 Nov 2017 22:10:18 GMT
CMD ["/bin/sh"]
# Sat, 04 Nov 2017 05:41:40 GMT
ENV LANG=C.UTF-8
# Sat, 04 Nov 2017 05:41:40 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 04 Nov 2017 05:41:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.7-openjdk
# Sat, 04 Nov 2017 05:41:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.7-openjdk/jre/bin:/usr/lib/jvm/java-1.7-openjdk/bin
# Sat, 04 Nov 2017 05:41:41 GMT
ENV JAVA_VERSION=7u131
# Sat, 04 Nov 2017 05:41:41 GMT
ENV JAVA_ALPINE_VERSION=7.131.2.6.9-r1
# Sat, 04 Nov 2017 05:41:52 GMT
RUN set -x 	&& apk add --no-cache 		openjdk7="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 04 Nov 2017 11:38:29 GMT
CMD ["gradle"]
# Sat, 04 Nov 2017 11:38:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 08 Nov 2017 20:07:54 GMT
ENV GRADLE_VERSION=4.3
# Wed, 08 Nov 2017 20:07:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=8dcbf44eef92575b475dcb1ce12b5f19d38dc79e84c662670248dc8b8247654c
# Wed, 08 Nov 2017 20:08:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8dcbf44eef92575b475dcb1ce12b5f19d38dc79e84c662670248dc8b8247654c
RUN set -o errexit -o nounset 	&& echo "Installing build dependencies" 	&& apk add --no-cache --virtual .build-deps 		ca-certificates 		openssl 		unzip 		&& echo "Downloading Gradle" 	&& wget -O gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip" 		&& echo "Checking download hash" 	&& echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c - 		&& echo "Installing Gradle" 	&& unzip gradle.zip 	&& rm gradle.zip 	&& mkdir /opt 	&& mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/" 	&& ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle 		&& apk del .build-deps 		&& echo "Adding gradle user and group" 	&& addgroup -S -g 1000 gradle 	&& adduser -D -S -G gradle -u 1000 -s /bin/ash gradle 	&& mkdir /home/gradle/.gradle 	&& chown -R gradle:gradle /home/gradle 		&& echo "Symlinking root Gradle cache to gradle Gradle cache" 	&& ln -s /home/gradle/.gradle /root/.gradle
# Wed, 08 Nov 2017 20:08:57 GMT
USER [gradle]
# Wed, 08 Nov 2017 20:08:57 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 08 Nov 2017 20:08:57 GMT
WORKDIR /home/gradle
# Wed, 08 Nov 2017 20:09:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8dcbf44eef92575b475dcb1ce12b5f19d38dc79e84c662670248dc8b8247654c
RUN set -o errexit -o nounset 	&& echo "Testing Gradle installation" 	&& gradle --version
```

-	Layers:
	-	`sha256:b56ae66c29370df48e7377c8f9baa744a3958058a766793f821dadcb144a4647`  
		Last Modified: Wed, 25 Oct 2017 23:21:25 GMT  
		Size: 2.0 MB (1991435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cebc5bcaf8176775fb87f51b16c709f4c03f3848a658c9a400facb452c7cdc`  
		Last Modified: Sat, 04 Nov 2017 05:58:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b523c1c6444e443426e81748ff890fec891bcce7b913e7324c0e2ac608dab06`  
		Last Modified: Sat, 04 Nov 2017 05:58:41 GMT  
		Size: 77.4 MB (77433041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f768ca2a0dbc5fc5fc9d88afdd967c95db05f27f2f05e35f0450990a7c667d`  
		Last Modified: Wed, 08 Nov 2017 20:19:11 GMT  
		Size: 73.4 MB (73366227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0498866c12d5e5df092cd4fb13217ab6dce9942a0e8426b7722e551234e4e3f`  
		Last Modified: Wed, 08 Nov 2017 20:19:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
