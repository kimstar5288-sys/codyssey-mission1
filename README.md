# Codyssey 미션 1
## 1. 프로젝트 개요

1) PowerShell 터미널을 사용하여 파일과 폴더를 생성하고,
  복사하고, 이동하고, 이름을 변경하고, 삭제하는 방법을 실습하였다.

2) Docker Desktop을 설치하고 기본 점검(버전확인 등), 기본 운영 명령수행,컨테이너 실행실습, 포트 매핑을 하였다.
3) Git 설정 및 Github 연동하였다.

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
- [x] 기본 운영명령 수행: 이미지, 컨테이너, 리소스 확인 등
- [x] Dockerfie 만들고 site 폴더안에 index.html 파일 생성
- [x] Docker이미지 만들기, 포트 매핑 접속
- [x] Docker 볼륨 영속성 검증

3) Git 설정 및 Github 연동 실습
- [x] Git 사용자 정보/기본 브랜치 설정 완료 등
- [x] Github 로그인과 저장소 연동
  

## 4. 수행로그
  1) 리눅스 터미널-  실습실행 결과: {첨부파일  리눅스 터미널 실습 로그.txt 참조)
* 현재위치확인
root@DESKTOP-FOK8PPV:~# pwd
/root

*일반목록
root@DESKTOP-FOK8PPV:~# ls
odyssey.practice  practice

* 상세목록
root@DESKTOP-FOK8PPV:~# ls -l
total 0
drwxr-xr-x 1 root root 512 Jul 28 01:56 odyssey.practice
drwxr-xr-x 1 root root 512 Jul 28 01:19 practice

* 숨은파일 목록
root@DESKTOP-FOK8PPV:~# ls -a
.  ..  .bash_history  .bashrc  .motd_shown  .profile  .ssh  odyssey.practice  practice


* 폴더 생성하기
root@DESKTOP-FOK8PPV:~# mkdir wsl-practice2
root@DESKTOP-FOK8PPV:~# ls
odyssey.practice  practice  wsl-practice  wsl-practice2

* 폴더 안으로 이동
root@DESKTOP-FOK8PPV:~# cd wsl-practice2
root@DESKTOP-FOK8PPV:~/wsl-practice2# pwd
/root/wsl-practice2
root@DESKTOP-FOK8PPV:~/wsl-practice2#

* 하위폴더 만들기
root@DESKTOP-FOK8PPV:~/wsl-practice2# mkdir backup
root@DESKTOP-FOK8PPV:~/wsl-practice2# ls
backup

* 빈 파일 만들기
root@DESKTOP-FOK8PPV:~/wsl-practice2# touch hello.txt
root@DESKTOP-FOK8PPV:~/wsl-practice2# ls -l
total 0
drwxr-xr-x 1 root root 512 Aug  1 11:32 backup
-rw-r--r-- 1 root root   0 Aug  1 11:34 hello.txt
root@DESKTOP-FOK8PPV:~/wsl-practice2#

* 파일에 내용 입력하기
root@DESKTOP-FOK8PPV:~/wsl-practice2# echo "Hello WSL" > hello.txt
root@DESKTOP-FOK8PPV:~/wsl-practice2# cat hello.txt
Hello WSL
root@DESKTOP-FOK8PPV:~/wsl-practice2#


* 파일 복사하기
root@DESKTOP-FOK8PPV:~/wsl-practice2# cp hello.txt hello-copy.txt
root@DESKTOP-FOK8PPV:~/wsl-practice2# ls -l
total 0
drwxr-xr-x 1 root root 512 Aug  1 11:32 backup
-rw-r--r-- 1 root root  10 Aug  1 11:38 hello-copy.txt
-rw-r--r-- 1 root root  10 Aug  1 11:36 hello.txt

* 파일 이름 변경하기
root@DESKTOP-FOK8PPV:~/wsl-practice2# mv hello-copy.txt renamed.txt
root@DESKTOP-FOK8PPV:~/wsl-practice2# ls
backup  hello.txt  renamed.txt

* 파일 이동하기
root@DESKTOP-FOK8PPV:~/wsl-practice2# mv renamed.txt backup/
root@DESKTOP-FOK8PPV:~/wsl-practice2# ls
backup  hello.txt

2) Docker Desktop 실습실행 결과
   {첨부파일  docker-terminal-log.txt 참조)
   {첨부파일  docker-desktop 화면.png 참조)
   (첨부파일  dockerfile-terminal-log.txt 첨조)
   (첨부파일 dockerimage-terminal-log.txt 참조)
   (첨부파일 docker image.png 참조)
   (첨부파일 dockervolume_terminal-log.txt 참조)

3) Git 설정 및 Github 연동 실습실행 결과
   (첨부파일 GitGithub연동-log-txt.txt참조)
   (참부파일 github 연동.png 참조)
   
## 5. 실습 결과
PowerShell 명령어를 사용하여 파일과 폴더를 직접 관리하는 방법을 익혔다.
Docker 기본 운영 명령을 익히고, 컨테이너 실행실습, Docker Image 만들기, 포트 매칭,Docker Volume 영속성 검증을 하였다.
Git설치와 Github 연동을 하였다.







 
>>>>>>> da8c91a634cdb158f961d3fa3a765709089745d3
