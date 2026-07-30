<<<<<<< HEAD

# Codyssey 미션 1

## 1. 프로젝트 개요

- PowerShell 터미널을 사용하여 파일과 폴더를 생성하고,
  복사하고, 이동하고, 이름을 변경하고, 삭제하는 방법을 실습하였다.
- Docker Desktop 설치 및 기본 점검, 기본운영명려웃행, 컨테이너 실행실습, Docker 이미지 제작, 포트 매필 및 접속, 볼륨 영속성 검증하였다.
- Git 설정 및 Github와 연동하였다.

## 2. 실행 환경

- 운영체제: Windows /WSL
- 터미널: PowerShell
- Shell: PowerShell

## 3. 수행 체크리스트

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

## 4. 현재 위치 확인

현재 작업 중인 폴더의 위치를 확인하였다.

```powershell
Get-Location
```

실행 결과:

```text
여기에 내 컴퓨터에서 나온 결과를 입력한다.
```

## 5. 목록 확인

현재 폴더의 파일과 폴더 목록을 확인하였다.

```powershell
Get-ChildItem
```

숨김 파일을 포함한 목록도 확인하였다.

```powershell
Get-ChildItem -Force
```

## 6. 폴더 생성 및 이동

`practice` 폴더를 생성하였다.

```powershell
New-Item -ItemType Directory -Name practice
```

생성한 폴더로 이동하였다.

```powershell
Set-Location practice
```

## 7. 빈 파일 생성

`empty.txt`라는 빈 파일을 생성하였다.

```powershell
New-Item -ItemType File -Name empty.txt
```

## 8. 파일 내용 작성 및 확인

`hello.txt` 파일에 문장을 저장하였다.

```powershell
"Codyssey Mission 1 PowerShell Practice" | Set-Content hello.txt
```

파일 내용을 확인하였다.

```powershell
Get-Content hello.txt
```

실행 결과:

```text
Codyssey Mission 1 PowerShell Practice
```

## 9. 파일 복사

`hello.txt`를 `hello-copy.txt`로 복사하였다.

```powershell
Copy-Item hello.txt hello-copy.txt
```

## 10. 파일 이름 변경

`hello-copy.txt` 파일의 이름을 `renamed.txt`로 변경하였다.

```powershell
Rename-Item hello-copy.txt renamed.txt
```

## 11. 파일 이동

`renamed.txt` 파일을 `backup` 폴더로 이동하였다.

```powershell
Move-Item renamed.txt backup
```

## 12. 파일 삭제

실습용 파일을 삭제하였다.

```powershell
Remove-Item delete-me.txt
```

## 13. 실습 결과

PowerShell 명령어를 사용하여 파일과 폴더를 직접 관리하는 방법을 익혔다.
=======

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

  

## 4. 수행로그
  1) Power Shell  터미널-  실습실행 결과: {첨부파일  터미널-terminal-log.txt 참조)
- 현재 위치 확인
  현재 작업 중인 폴더의 위치를 확인하였다.

```powershell
Get-Location
```

-목록 확인
현재 폴더의 파일과 폴더 목록을 확인하였다.

```powershell
Get-ChildItem
```

숨김 파일을 포함한 목록도 확인하였다.

```powershell
Get-ChildItem -Force
```

- 폴더 생성 및 이동
`practice` 폴더를 생성하였다.

```powershell
New-Item -ItemType Directory -Name practice
```

생성한 폴더로 이동하였다.

```powershell
Set-Location practice
```

- 빈 파일 생성

`empty.txt`라는 빈 파일을 생성하였다.

```powershell
New-Item -ItemType File -Name empty.txt
```

- 파일 내용 작성 및 확인

`hello.txt` 파일에 문장을 저장하였다.

```powershell
"Codyssey Mission 1 PowerShell Practice" | Set-Content hello.txt
```

파일 내용을 확인하였다.

```powershell
Get-Content hello.txt
```


- 파일 복사

`hello.txt`를 `hello-copy.txt`로 복사하였다.

```powershell
Copy-Item hello.txt hello-copy.txt
```

- 파일 이름 변경

`hello-copy.txt` 파일의 이름을 `renamed.txt`로 변경하였다.

```powershell
Rename-Item hello-copy.txt renamed.txt
```

- 파일 이동

`renamed.txt` 파일을 `backup` 폴더로 이동하였다.

```powershell
Move-Item renamed.txt backup
```

- 파일 삭제
실습용 파일을 삭제하였다.

```powershell
Remove-Item delete-me.txt
```

2) Docker Desktop 실습실행 결과
   {첨부파일  docker-terminal-log.txt 참조)
   {첨부파일  docker-desktop 화면.png 참조)
   (첨부파일  dockerfile-terminal-log.txt 첨조)
   (첨부파일 dockerimage-terminal-log.txt 참조)
   (첨부파일 docker image.png 참조)
   (첨부파일 dockervolume_terminal-log.txt 참조)
   
4) 실습 결과
PowerShell 명령어를 사용하여 파일과 폴더를 직접 관리하는 방법을 익혔다.
Docker 기본 운영 명령을 익히고, 컨테이너 실행실습, Docker Image 만들기, 포트 매칭,Docker Volume 영속성 검증을 하였다.








 
>>>>>>> da8c91a634cdb158f961d3fa3a765709089745d3
