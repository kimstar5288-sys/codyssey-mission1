
# Codyssey 미션 1
[ PowerShell 터미널 기본 조작 실습]
## 1. 프로젝트 개요

PowerShell 터미널을 사용하여 파일과 폴더를 생성하고,
복사하고, 이동하고, 이름을 변경하고, 삭제하는 방법을 실습하였다.

## 2. 실행 환경

- 운영체제: Windows
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
