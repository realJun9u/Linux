# Linux  
---
## 명령어  
---  
- whoami : 현재 유저명 출력  

- pwd : 현재 디렉토리 출력  

- ls : 파일 리스트 출력  
```
 -l : 상세 정보  
 -a : 숨김 파일  
 -S : 파일 크기순 정렬  
 -R : 디렉토리 아래의 모든 파일 출력  
```
- mkdir : 디렉토리 생성 
```
-p : 부모 디렉토리 함께 생성  
```
- touch : 빈 파일 생성  

- cd : 디렉토리 이동  
```
../  : 상위 디렉토리 (/ 생략 가능)  
  ~ : 홈 디렉토리  
  / : 루트 디렉토리  
```
- rm : 파일 삭제
``` 
  -r : 재귀적 삭제 (디렉토리 삭제)  
  -i : interactive  
```
- cp {원본} {사본} : 파일 복사  

- mv {파일} {목적지} : 파일 이동  

- cat : 파일 내용 출력  

- head : 파일 내용 윗 부분 출력  

- tail : 파일 내용 밑 부분 출력  
```
-f : 파일 내용에 실시간으로 추가되는 내용 출력  
```
- grep : 파일에서 특정 문자열이 포함된 행 출력  

- basename : 경로+파일명에서 경로와 확장자를 제거한 파일 이름만 출력

- dirname : 경로+파일명에서 경로만 출력

- chmod : 파일 권한 변경  

- chown : 파일 소유자,그룹 변경  
```
  -R : 디렉토리 아래의 모든 파일 권한 변경  
```
- alias : 별칭 지정  

- sudo : 루트 권한 사용  

- su : 유저 변경  
```
su - root : 슈퍼 유저로 변경  
```
- passwd : 유저 패스워드 변경  
```
  -u root : 루트 유저 언락  
  -l root : 루트 유저 락  
```
- useradd : 유저 추가
```
-m : 홈 디렉토리도 생성  
```
- usermod : 유저 계정 수정 
```
  -a -G : 그룹에 유저 추가 ( -a -G 함께 사용 )  
  예) sudo usermod -a -G sudo newuser = 유저를 sudo 그룹에 추가  
```  
- userdel : 유저 삭제  

- adduser : 향상된 유저 추가  

- deluser : 향상된 유저 삭제  

- nano : nano 에디터 사용  

- vim : vim 에디터 사용  

- ps : 실행중인 프로세스 목록/상태  
```
  a : 터미널에서 실행한 프로세스 정보 출력  
  x : 실행 중인 모든 프로세스 정보 출력  
  u : 프로세스 소유자 이름, CPU 사용량, 메모리 사용량 등 상세 정보 출력  
  f : Show process hierarchy in forest format  
  w : wide format 출력  
  -e : 실행중인 모든 프로세스 정보 출력 (ax와 유사)  
  -f : 프로세스에 대한 상세 정보 출력 (u와 유사 PPID(부모 프로세스 번호) 확인 가능)  
  axf == -e --forest  
  -o [Option]... : 출력 정보 추가  
```  
- nice : 프로세스가 실행될 때 실행 우선순위(NI) 조정. -20 ~ 19 -20이 우선순위가 가장 높다. 일반 유저는 값을 증가만 할 수 있다. nice [-n 수치] [프로세스]

- renice : 실행중인 프로세스에 대한 nice 값 변경. renice [옵션] [수치] [PID]  

- top : 실행중인 프로세스 정보 (ps와 유사)  

- locate : 파일을 데이터베이스에서 검색  

- find : 파일을 디렉토리를 돌며 검색  

- whereis : 실행, 소스, 매뉴얼 파일의 경로(위치)를 검색  

- jobs : 백그라운드 프로그램 목록 (Ctrl+z로 백그라운드 사용)  

- crontab : 정기적인 명령 처리  

- rsync : 원격으로 독립된 컴퓨터 사이 파일 관리  
```
  -a : archive 모드. 디렉토리 전체 복사, 변경 사항, 파일 속성 전송 (많은 기능)
  -v : verbose 모드
```
- curl ipinfo.io/ip : public ip 확인  

- ip addr : private ip 확인  

- [ufw](https://webdir.tistory.com/206) : 방화벽 설정 (iptables 관리 수월)  

- host {도메인} : 도메인의 ip 확인  

- apt : apt 패키지 매니저  
> -get  
```
   update : 목록 최신화  
   install : 설치  
   upgrade : 설치된 패키지 최신화
   remove : 삭제 (패키지)  
   purge : 삭제 (패키지 + 설정 파일)  
```   
> -cache  
```
   search : 패키지 검색  
   pkgnames : 설치할 수 있는 패키지 목록  
```
- wget {URL} : URL을 통해서 다운로드  
```
  -O : 다른 이름으로 저장  
```
- git : 버전 관리 시스템. 개발/관리에 필요
> 예) git clone {소스코드 주소} {저장할 디렉토리 이름} : Github의 소스코드 다운로드

## 패키지/서비스(데몬)  
- elinks : 웹 브라우저 프로그램 
- apache2 : 웹 서버 프로그램  
- htop : top 명령어의 graphical한 버전  
- ifconfig : private ip 확인  
- ssh : 쉘을 통해 제어하는 서버,클라이언트의 원격 통신  
> openssh-server : ssh를 사용하기 위한 서버 패키지  
  openssh-client : ssh를 사용하기 위한 클라이언트 패키지  

## 유용한 기능
1. sequence execution ( ; ) : 여러 명령을 순차적으로 실행시킬 때 사용  
2. piping ( | ) : 한 명령의 출력을 다른 명령의 인자로 전환  
3. redirection ( > ) : 표준 출력, 에러를 파일 출력으로 전환  
> 리눅스에서 프로그램(프로세스) 실행시 기본적으로 3개의 스트림이 자동적으로 열린다. 입력을 위한 스트림 (Standard input, stdin), 출력을 위한 스트림 (Standard output, stdout), 오류 메시지 출력을 위한 스트림 (Standard error, stderr)이며, 이를 표준 스트림이라고 부른다.  
4. background ( Ctrl+z, & ) : 백그라운드 실행을 통해 하던 작업을 두고 다른 작업을 할 수 있다.  
> Ctrl+z : 프로그램 실행 중 CTRL+Z를 통하여 현재 프로그램을 백그라운드에서 실행 되도록 한다.  
  & : 프로그램 실행 시 끝에 &를 붙여 백그라운드로 실행 시킬 수 있음  
  fg 명령을 통해 포그라운드로 불러올 수 있다. 이 때 % 다음의 숫자는 stopped 앞의 대괄호 숫자 값  
  jobs 명령을 통해 현재 백그라운드에서 동작하고 있는 프로그램의 확인  
  kill (-9) % 명령을 통해 백그라운드에서 동작하고 있는 프로그램을 종료 (-9는 강제 종료)  



## 내용 참고
1. [Directory Structure](https://www.thegeekstuff.com/2010/09/linux-file-system-structure/)  
2. [Startup Script]  
3. 한국 통신사가 제공하는 케이블, 와이파이 접속하는 순간 /etc/resolve.conf 의 ip가 바뀜.  

