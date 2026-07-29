
# Codyssey 미션 1
## 1. 프로젝트 개요

1) PowerShell 터미널을 사용하여 파일과 폴더를 생성하고,
  복사하고, 이동하고, 이름을 변경하고, 삭제하는 방법을 실습하였다.

2) Docker Desktop을 섪치하고 기본 점검(버전확인 등), 기본 운영 명령수행을 하였다.

## 2. 실행 환경

- 운영체제: Windows / WSL2
- 터미널: PowerShell
- Shell: PowerShell

## 3. 수행 체크리스트
1) Power Shell  터미널 실습
- [x] 현재 위치 확인
- [x] 파일과 폴더 목록 확인
- [x] 숨김 파일 포함 목록 확인
- [x] 폴더 이동
- [x] 폴더 생성
- [x] 빈 파일 생성
- [x] 파일 복사
- [x] 파일 이름 변경
- [x] 파일 이동
- [x] 파일 삭제
- [x] 파일 내용 확인

2) Docker Desktop 실습
- [x] 버전확인
- [x] 데몬 동작여부 확인
- [x] 기본 운영명령 수행: 이미지, 컨테이너, 리소스 확인 등

## 4. 수행로그
1) Power Shell  터미널-  실습실행 결과: {하단부 로그 내용에서 제시)
- 현재 위치 확인
  현재 작업 중인 폴더의 위치를 확인하였다.

```powershell
Get-Location
```

2) 목록 확인
현재 폴더의 파일과 폴더 목록을 확인하였다.

```powershell
Get-ChildItem
```

숨김 파일을 포함한 목록도 확인하였다.

```powershell
Get-ChildItem -Force
```

3) 폴더 생성 및 이동
`practice` 폴더를 생성하였다.

```powershell
New-Item -ItemType Directory -Name practice
```

생성한 폴더로 이동하였다.

```powershell
Set-Location practice
```

4) 빈 파일 생성

`empty.txt`라는 빈 파일을 생성하였다.

```powershell
New-Item -ItemType File -Name empty.txt
```

5) 파일 내용 작성 및 확인

`hello.txt` 파일에 문장을 저장하였다.

```powershell
"Codyssey Mission 1 PowerShell Practice" | Set-Content hello.txt
```

파일 내용을 확인하였다.

```powershell
Get-Content hello.txt
```


6) 파일 복사

`hello.txt`를 `hello-copy.txt`로 복사하였다.

```powershell
Copy-Item hello.txt hello-copy.txt
```

7) 파일 이름 변경

`hello-copy.txt` 파일의 이름을 `renamed.txt`로 변경하였다.

```powershell
Rename-Item hello-copy.txt renamed.txt
```

8) 파일 이동

`renamed.txt` 파일을 `backup` 폴더로 이동하였다.

```powershell
Move-Item renamed.txt backup
```

9) 파일 삭제

실습용 파일을 삭제하였다.

```powershell
Remove-Item delete-me.txt
```

10) 실습 결과

PowerShell 명령어를 사용하여 파일과 폴더를 직접 관리하는 방법을 익혔다.

<Power Shell 기록>
**********************
Windows PowerShell 기록 시작
시작 시간: 20260728155342
사용자 이름: DESKTOP-FOK8PPV\김성완
RunAs 사용자: DESKTOP-FOK8PPV\김성완
구성 이름: 
Machine: DESKTOP-FOK8PPV (Microsoft Windows NT 10.0.19045.0)
호스트 응용 프로그램: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
프로세스 ID: 22900
PSVersion: 5.1.19041.6456
PSEdition: Desktop
PSCompatibleVersions: 1.0, 2.0, 3.0, 4.0, 5.0, 5.1.19041.6456
BuildVersion: 10.0.19041.6456
CLRVersion: 4.0.30319.42000
WSManStackVersion: 3.0
PSRemotingProtocolVersion: 2.3
SerializationVersion: 1.1.0.1
**********************
기록이 시작되었습니다. 출력 파일은 terminal-log.txt입니다.
PS C:\Users\김성완\Documents\codyssey-mission1> Get-Location

Path
----
C:\Users\김성완\Documents\codyssey-mission1


PS C:\Users\김성완\Documents\codyssey-mission1> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 3:53            733 terminal-log.txt


PS C:\Users\김성완\Documents\codyssey-mission1> Get-ChildItem -Force


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 3:53            733 terminal-log.txt


PS C:\Users\김성완\Documents\codyssey-mission1> New-Item -ItemType File -Name hidden.txt


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 4:04              0 hidden.txt


PS C:\Users\김성완\Documents\codyssey-mission1> (Get-Item hidden.txt).Attributes = "Hidden"
PS C:\Users\김성완\Documents\codyssey-mission1> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 3:53            733 terminal-log.txt


PS C:\Users\김성완\Documents\codyssey-mission1> Get-ChildItem -Force


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
---h--      2026-07-28   오후 4:04              0 hidden.txt
-a----      2026-07-28   오후 3:53            733 terminal-log.txt


PS C:\Users\김성완\Documents\codyssey-mission1> New-Item -ItemType Directory -Name practice


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:06                practice


PS C:\Users\김성완\Documents\codyssey-mission1> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:06                practice
-a----      2026-07-28   오후 4:06           3037 terminal-log.txt


PS C:\Users\김성완\Documents\codyssey-mission1> Set-Location practice
PS C:\Users\김성완\Documents\codyssey-mission1\practice> cd ..
PS C:\Users\김성완\Documents\codyssey-mission1> cd practice
PS C:\Users\김성완\Documents\codyssey-mission1\practice> New-Item -ItemType File -Name empty.txt


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 4:14              0 empty.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 4:14              0 empty.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> "Codyssey Mission 1 PowerShell Practice" | Set-Content hello.txt
PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 4:14              0 empty.txt
-a----      2026-07-28   오후 4:15             40 hello.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-Content hello.txt
Codyssey Mission 1 PowerShell Practice
PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-Content empty.txt
PS C:\Users\김성완\Documents\codyssey-mission1\practice> Copy-Item hello.txt hello-copy.txt
PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 4:14              0 empty.txt
-a----      2026-07-28   오후 4:15             40 hello-copy.txt
-a----      2026-07-28   오후 4:15             40 hello.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-Content hello-copy.txt
Codyssey Mission 1 PowerShell Practice
PS C:\Users\김성완\Documents\codyssey-mission1\practice> Rename-Item hello-copy.txt renamed.txt
PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 4:14              0 empty.txt
-a----      2026-07-28   오후 4:15             40 hello.txt
-a----      2026-07-28   오후 4:15             40 renamed.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-Content renamed.txt
Codyssey Mission 1 PowerShell Practice
PS C:\Users\김성완\Documents\codyssey-mission1\practice> New-Item -ItemType Directory -Name backup


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:26                backup


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Move-Item renamed.txt backup
PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:26                backup
-a----      2026-07-28   오후 4:14              0 empty.txt
-a----      2026-07-28   오후 4:15             40 hello.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem backup


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 4:15             40 renamed.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-Content backup\renamed.txt
Codyssey Mission 1 PowerShell Practice
PS C:\Users\김성완\Documents\codyssey-mission1\practice> New-Item -ItemType File -Name delete-me.txt


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 4:30              0 delete-me.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:26                backup
-a----      2026-07-28   오후 4:30              0 delete-me.txt
-a----      2026-07-28   오후 4:14              0 empty.txt
-a----      2026-07-28   오후 4:15             40 hello.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Remove-Item delete-me.txt
PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:26                backup
-a----      2026-07-28   오후 4:14              0 empty.txt
-a----      2026-07-28   오후 4:15             40 hello.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> New-Item -ItemType Directory -Name delete-folder


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:31                delete-folder


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:26                backup
d-----      2026-07-28   오후 4:31                delete-folder
-a----      2026-07-28   오후 4:14              0 empty.txt
-a----      2026-07-28   오후 4:15             40 hello.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Remove-Item delete-folder
PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:26                backup
-a----      2026-07-28   오후 4:14              0 empty.txt
-a----      2026-07-28   오후 4:15             40 hello.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-Location

Path
----
C:\Users\김성완\Documents\codyssey-mission1\practice


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem -Force


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:26                backup
-a----      2026-07-28   오후 4:14              0 empty.txt
-a----      2026-07-28   오후 4:15             40 hello.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Get-ChildItem -Recurse -Force


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2026-07-28   오후 4:26                backup
-a----      2026-07-28   오후 4:14              0 empty.txt
-a----      2026-07-28   오후 4:15             40 hello.txt


    디렉터리: C:\Users\김성완\Documents\codyssey-mission1\practice\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2026-07-28   오후 4:15             40 renamed.txt


PS C:\Users\김성완\Documents\codyssey-mission1\practice> Stop-Transcript
**********************
Windows PowerShell 기록 끝
종료 시간: 20260728163426
**********************

<Docker Desktop 기록>
Windows PowerShell 기록 시작
시작 시간: 20260729123917
사용자 이름: DESKTOP-FOK8PPV\김성완
RunAs 사용자: DESKTOP-FOK8PPV\김성완
구성 이름: 
Machine: DESKTOP-FOK8PPV (Microsoft Windows NT 10.0.19045.0)
호스트 응용 프로그램: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
프로세스 ID: 9544
PSVersion: 5.1.19041.6456
PSEdition: Desktop
PSCompatibleVersions: 1.0, 2.0, 3.0, 4.0, 5.0, 5.1.19041.6456
BuildVersion: 10.0.19041.6456
CLRVersion: 4.0.30319.42000
WSManStackVersion: 3.0
PSRemotingProtocolVersion: 2.3
SerializationVersion: 1.1.0.1
**********************
기록이 시작되었습니다. 출력 파일은 terminal-log.txt입니다.
PS C:\Users\김성완> docker --version
Docker version 29.6.2, build dfc4efb
PS C:\Users\김성완> docker info
Client:
 Version:    29.6.2
 Context:    desktop-linux
 Debug Mode: false
 Plugins:
  agent: Docker AI Agent Runner (Docker Inc.)
    Version:  v1.111.0
    Path:     C:\Program Files\Docker\cli-plugins\docker-agent.exe
  ai: Docker AI Agent - Ask Gordon (Docker Inc.)
    Version:  v1.27.0
    Path:     C:\Program Files\Docker\cli-plugins\docker-ai.exe
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.35.0-desktop.2
    Path:     C:\Program Files\Docker\cli-plugins\docker-buildx.exe
  compose: Docker Compose (Docker Inc.)
    Version:  v5.3.1
    Path:     C:\Program Files\Docker\cli-plugins\docker-compose.exe
  debug: Get a shell into any image or container (Docker Inc.)
    Version:  0.0.47
    Path:     C:\Program Files\Docker\cli-plugins\docker-debug.exe
  desktop: Docker Desktop commands (Docker Inc.)
    Version:  v0.4.3
    Path:     C:\Program Files\Docker\cli-plugins\docker-desktop.exe
  dhi: CLI for managing Docker Hardened Images (Docker Inc.)
    Version:  v0.0.7
    Path:     C:\Program Files\Docker\cli-plugins\docker-dhi.exe
  extension: Manages Docker extensions (Docker Inc.)
    Version:  v0.2.31
    Path:     C:\Program Files\Docker\cli-plugins\docker-extension.exe
  init: Creates Docker-related starter files for your project (Docker Inc.)
    Version:  v1.4.0
    Path:     C:\Program Files\Docker\cli-plugins\docker-init.exe
  mcp: Docker MCP Plugin (Docker Inc.)
    Version:  v0.43.3
    Path:     C:\Program Files\Docker\cli-plugins\docker-mcp.exe
  model: Docker Model Runner (Docker Inc.)
    Version:  v1.2.6
    Path:     C:\Program Files\Docker\cli-plugins\docker-model.exe
  offload: Docker Offload (Docker Inc.)
    Version:  v0.6.9
    Path:     C:\Program Files\Docker\cli-plugins\docker-offload.exe
  pass: Docker Pass Secrets Manager Plugin (beta) (Docker Inc.)
    Version:  v0.2.0
    Path:     C:\Program Files\Docker\cli-plugins\docker-pass.exe
  sandbox: "docker sandbox" is deprecated, use Docker Sandboxes instead (Docker Inc.)
    Version:  v0.13.0
    Path:     C:\Program Files\Docker\cli-plugins\docker-sandbox.exe
  scout: Docker Scout (Docker Inc.)
    Version:  v1.23.1
    Path:     C:\Program Files\Docker\cli-plugins\docker-scout.exe

Server:
 Containers: 0
  Running: 0
  Paused: 0
  Stopped: 0
 Images: 0
 Server Version: 29.6.2
 Storage Driver: overlayfs
  driver-type: io.containerd.snapshotter.v1
 Logging Driver: json-file
 Cgroup Driver: cgroupfs
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 CDI spec directories:
  /etc/cdi
  /var/run/cdi
 Discovered Devices:
  cdi: docker.com/gpu=webgpu
 Swarm: inactive
 Runtimes: io.containerd.runc.v2 nvidia runc
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: e53c7c1516c3b2bff98eb76f1f4117477e6f4e66
 runc version: v1.3.6-0-g491b69ba
 init version: de40ad0
 Security Options:
  seccomp
   Profile: builtin
  cgroupns
 Kernel Version: 6.18.33.2-microsoft-standard-WSL2
 Operating System: Docker Desktop
 OSType: linux
 Architecture: x86_64
 CPUs: 4
 Total Memory: 3.78GiB
 Name: docker-desktop
 ID: 32f9fabd-2f9e-4e0d-a355-085b5bbe69bf
 Docker Root Dir: /var/lib/docker
 Debug Mode: false
 HTTP Proxy: http.docker.internal:3128
 HTTPS Proxy: http.docker.internal:3128
 No Proxy: hubproxy.docker.internal
 Labels:
  com.docker.desktop.address=npipe://\\.\pipe\docker_cli
 Experimental: false
 Insecure Registries:
  hubproxy.docker.internal:5555
  ::1/128
  127.0.0.0/8
 Live Restore Enabled: false
 Firewall Backend: iptables
PS C:\Users\김성완> docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
4f55086f7dd0: Pull complete
d5e71e642bf5: Download complete
Digest: sha256:c3cbe1cc1aa588a64951ac6286e0df7b27fe2e6324b1001c619bb358770c0178
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
PS C:\Users\김성완> docker images
                                                                                                   i Info →    U  In Use
IMAGE                ID             DISK USAGE   CONTENT SIZE   EXTRA
hello-world:latest   c3cbe1cc1aa5       25.9kB         9.49kB    U
PS C:\Users\김성완> docker ps -a
CONTAINER ID   IMAGE         COMMAND    CREATED         STATUS                     PORTS     NAMES
057a2501349b   hello-world   "/hello"   7 minutes ago   Exited (0) 5 minutes ago             pedantic_turing
PS C:\Users\김성완> docker run --name hello-test hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
PS C:\Users\김성완> docker stats --no-stream

PS C:\Users\김성완> dpcker ststs --no-stream
dpcker : 'dpcker' 용어가 cmdlet, 함수, 스크립트 파일 또는 실행할 수 있는 프로그램 이름으로 인식되지 않습니다. 이름이 정확한지 확인하고 경로가 포함된 경우 경로가 올바른지 검증한 다음 다시 시
도하십시오.
위치 줄:1 문자:1
+ dpcker ststs --no-stream
+ ~~~~~~
    + CategoryInfo          : ObjectNotFound: (dpcker:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
dpcker : 'dpcker' 용어가 cmdlet, 함수, 스크립트 파일 또는 실행할 수 있는 프로그램 이름으로 인식되지 않습니다. 이름이 정
확한지 확인하고 경로가 포함된 경우 경로가 올바른지 검증한 다음 다시 시도하십시오.
위치 줄:1 문자:1
+ dpcker ststs --no-stream
+ ~~~~~~
    + CategoryInfo          : ObjectNotFound: (dpcker:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException

PS C:\Users\김성완> docker stats --no-stream

PS C:\Users\김성완> docker run -it --name ubuntu-test ubuntu bash
Unable to find image 'ubuntu:latest' locally
latest: Pulling from library/ubuntu
a3679419df18: Pull complete
ed819469700f: Pull complete
e16351a257e4: Download complete
Digest: sha256:3131b4cc82a783df6c9df078f86e01819a13594b865c2cad47bd1bca2b7063bb
Status: Downloaded newer image for ubuntu:latest
root@a1bd4d51a982:/# pwd
/
root@a1bd4d51a982:/# Is
bash: Is: command not found
root@a1bd4d51a982:/# is
bash: is: command not found
root@a1bd4d51a982:/# echo "hello Ubuntu"
hello Ubuntu
root@a1bd4d51a982:/# exit
exit
PS C:\Users\김성완> docker ps -q

PS C:\Users\김성완> docker ps -a
CONTAINER ID   IMAGE         COMMAND    CREATED              STATUS                      PORTS     NAMES
a1bd4d51a982   ubuntu        "bash"     About a minute ago   Exited (0) 29 seconds ago             ubuntu-test
d86e8cf76c2a   hello-world   "/hello"   29 minutes ago       Exited (0) 29 minutes ago             hello-test
057a2501349b   hello-world   "/hello"   41 minutes ago       Exited (0) 41 minutes ago             pedantic_turing
PS C:\Users\김성완> docker start ubuntu-test
ubuntu-test
PS C:\Users\김성완> docker exec -it ubuntu-test bash
root@a1bd4d51a982:/# exit
exit

What's next:
    Try Docker Debug for seamless, persistent debugging tools in any container or image →  docker debug ubuntu-test
    Learn more at https://docs.docker.com/go/debug-cli/
PS C:\Users\김성완> Stop-Transcript
**********************
Windows PowerShell 기록 끝
종료 시간: 20260729132622
**********************
