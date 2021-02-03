# Linux  
---
## 명령어  
---  
- whoami : 현재 유저명 출력  
- pwd : 현재 디렉토리 출력  
- ls : 파일 리스트 출력  
> -l : 상세 정보  
  -a : 숨김 파일  
  -S : 파일 크기순 정렬  
  -R : 디렉토리 아래의 모든 파일 출력
- mkdir : 디렉토리 생성 
> -p : 부모 디렉토리 함께 생성  
- touch : 빈 파일 생성  
- cd : 디렉토리 이동  
> ../  : 상위 디렉토리 (/ 생략 가능)  
  ~ : 홈 디렉토리  
  / : 루트 디렉토리  
- rm : 파일 삭제
> -r : 재귀적 삭제 (디렉토리 삭제)  
  -i : interactive  
- cp {원본} {사본} : 파일 복사  
- mv {파일} {목적지} : 파일 이동  
- cat : 파일 내용 출력  
- grep : 파일에서 특정 문자열이 포함된 행 출력  
- sudo : 루트 권한 사용  
- nano : nano 에디터 사용  
- vim : vim 에디터 사용  
- ps : 실행중인 프로세스 목록/상태  
> aux : 실행중인 모든 프로세스 정보  
- top : 실행중인 프로세스 정보 (ps와 유사)  
- htop : top 명령어의 graphical한 버전  
- locate : 파일을 데이터베이스에서 검색  
- find : 파일을 디렉토리를 돌며 검색  
- whereis : 실행, 소스, 매뉴얼 파일의 경로(위치)를 검색  
- jobs : 백그라운드 프로그램 목록 (Ctrl+z로 백그라운드 사용)  
- apt : apt 패키지 매니저  
> -get  
>   > update : 목록 최신화  
      install : 설치  
      upgrade : 설치된 패키지 최신화
      remove : 삭제 (패키지)  
      purge : 삭제 (패키지 + 설정 파일)  
      
>  -cache  
>   > search : 패키지 검색  
      pkgnames : 설치할 수 있는 패키지 목록  
- wget {URL} : URL을 통해서 다운로드  
> -O : 다른 이름으로 저장  

- git : 버전 관리 시스템. 개발/관리에 필요
> 예) git clone {소스코드 주소} {저장할 디렉토리 이름} : Github의 소스코드 다운로드

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
2. 

