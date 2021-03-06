## `python:2-windowsservercore`

```console
$ docker pull python@sha256:f1fa25481530503795860dd213c91270344d25f77652c8f9a9de9696f734a702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1884; amd64

### `python:2-windowsservercore` - windows version 10.0.14393.1884; amd64

```console
$ docker pull python@sha256:14af796f9ef8d781f1a8968ff1b45c78a97bbde838a65f660b2a96cfed07e302
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5411053981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8666922f9b7f0d01cbbf1a5b27a7fa3ccaf6733ad4f1e7d8415837e7c2fe71e7`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 13 Nov 2017 21:42:13 GMT
RUN Install update 10.0.14393.1884
# Wed, 15 Nov 2017 03:14:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Nov 2017 17:38:37 GMT
ENV PYTHON_VERSION=2.7.14
# Wed, 15 Nov 2017 17:38:38 GMT
ENV PYTHON_RELEASE=2.7.14
# Wed, 15 Nov 2017 17:40:39 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Nov 2017 17:40:40 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Wed, 15 Nov 2017 17:42:21 GMT
RUN Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri 'https://bootstrap.pypa.io/get-pip.py' -OutFile 'get-pip.py'; 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Wed, 15 Nov 2017 17:43:30 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 15 Nov 2017 17:43:31 GMT
CMD ["python"]
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
	-	`sha256:a4bd6cd94ee2a374930b7554f113d83a6d2d7c4fc6059acd6f2f60e0f29d2f26`  
		Last Modified: Wed, 15 Nov 2017 10:26:12 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71618351f5fe4210bca5134933d01439c7747b5d984c5041b56392fa011e4dc3`  
		Last Modified: Wed, 15 Nov 2017 17:45:14 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004619ac3e10ad6ef5274a30aa8549c55951b0e9c2d8baf4a8343eccdabf47f0`  
		Last Modified: Wed, 15 Nov 2017 17:45:14 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2949cf2a1d52ebd916ccd050d6b0f14c50d060343ab045e0fbc1ac52c43d73`  
		Last Modified: Wed, 15 Nov 2017 17:45:24 GMT  
		Size: 38.4 MB (38355786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89447017b8cf8e79074052c82bbb7e5c60dfe46591f4bd3b738f6f010bd587a9`  
		Last Modified: Wed, 15 Nov 2017 17:45:10 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd71a2d446e1138ce6b87a4398b8ccdd37c0288e0d5e0354e14914680b1c843`  
		Last Modified: Wed, 15 Nov 2017 17:45:16 GMT  
		Size: 9.0 MB (8990477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1e60bb19035159ac490c1003066f4f080ea2ffdad34f1af4e540dd4ead36bc`  
		Last Modified: Wed, 15 Nov 2017 17:45:13 GMT  
		Size: 6.7 MB (6722838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c4123abcb661eafbf6bc919e86c6e6593f966e24395fc600a5fd80105b070f`  
		Last Modified: Wed, 15 Nov 2017 17:45:10 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
