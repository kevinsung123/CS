### find
- escape 방법 2가지
	1. \;
	2. ";" 
- find . -name  * -exec ls -a {} \;
	- { } : find의 output이다 


예제1)
$ find . -name "*.html" -type f -ls
> 현재디렉토리이하에 확장자가 html인 파일만 찾기

예제2)
$ find . -size +300k -ls
> 파일크기가 300kb이상인 파일만

예제3)
 >  + ; / 차이
 $ find . -type f -exec chmod 775 {} +  
chmod 775 fileA fileB fileC
=> xargs와 유사
 
- $ find . -type f -exec chmod 775 {} \;
chmod 775 fileA
chmod 775 fileB
chmod 775 fileC
`
-  수정일 
```
$ find ./ -mtime +20 -ls 
>수정한지 20일이상된 파일과 디렉토리

$ find ./ -mtime +20 -typle f -ls 
>수정한지 20일이상된 파일

$ find . -mtime +20 -type f -ls -exec rm {} \;
>수정한지 20일이상된 파일만 삭제
```
- 출력 형식지정
-  %h=경로  %f=파일명 %k=KB %s=Bytes
-  형식 : <경로/파일명> <파일크기KB>
> find ./ -printf "%h/%f\t %kKB \n"

### df
- 리눅스 시스템의 마운트 된 디스크 사용량을 확인
- 파일시스템 / 디스크크기 / 사용량 /여유공간 /사용률 /마운트지점
- h 옵션 : humanable 사람이 보기좋게 M,G 단위로 확인
### du
- disk usage : 디렉토리 디스크 사용량 확인
- 특정 디렉토리 기준으로 디스크사용량 확인
-  h 옵션 가능
-  s 옵션은 용약된 정보

### ls

- ls --time-style="+%Y-%m-%d %H:%M:%S -alt | grep ^- | more
- 파일명 기준 내림차순 : ls -lr
- 특정 디렉토리 모든파일 확인 : ls-al
- 용량별로 내림차순 : ls -lS
- 용량별로 오름차순 : ls -lSr
- 시간순서대로 표시  : ls -lt
- 사용시간 순서대로 표시 : ls -lU
- 파일크기 내림차순 : ls -alSh
