### journalctl이란?
- systemd의 서비스로그 확인가능
- systemd-journald.serivce에 의해서 정보들을 분석
- 옵션
	- a : 모든 log 출력
	- b : 마지막부팅후 log만 출력
	- f : 가장 최근 log 표시 및 실시간
	```
	- 오늘날짜로그
	# journalctl --since=today
	- 특정기간로그
	# journalctl --since "2017-05-25 00:00:00" --until "2017-05-30 00:00:00"
	- 특정 서비스 데몬 로그 보기
	# journalctl -u sshd
	- 특정 이벤트 속성 조회
	# journalctl -p crit 
	``` 
### systemctl 사용법
- 부팅 속도 체크
**> #systemd-analyze** 
- 서비스 목록 확인 (등록된 모든 서비스)
**> #systemctl list-unit-files**
- 서비스간 의존관계 (dependency)
**>  #systemctl list-dependencies mariadb.service**
- unit file
**> 기본적으로 /usr/lib/system  디렉토리에 unitfile보관.**
**> 보통 service확장자를 가짐**
- 모든서비스 확인
**> systemctl list-units --type service --all**
- 서비스 만들기 
> [enter link description here](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/sect-managing_services_with_systemd-unit_files)
- 서비스 마스킹
	- 동일한 용도로 사용하는 서비스가 동시에 설치되어있는경우 충돌가능
	**>sudo systemctl mask ntpd => masking처리** 
- 모든 active 목록
**> sudo systemctl list-units --state=active**
 
	1. 서비스 활성화
	**# systemctl enable <서비스명>**
	2. 서비스 비활성화
	**# systemctl disable <서비스명>**
	3. 서비스 시작
	**# systemctl start <서비스명>**
	4. 서비스 종료
	**# systemctl stop <서비스명>**
	5. 서비스 재시작
	**# systemctl restart <서비스명>**

	6. 서비스 갱신
	**# systemctl reload <서비스명>**
	7. 실패 서비스 확인
	**# systemctl --failed**
	8. 서비스 설정을 데몬에 반영시
	**# systemctl daemon-reload**
	9. 서비스와 관련된 프로세스 모두 죽일때
	**# systemctl kill <서비스명>**
	10. 서비스의 자세한 상태
	**# systemctl status -l <서비스명>**
-	출처: [https://flyyunha.tistory.com/entry/systemctl-사용법?category=564154](https://flyyunha.tistory.com/entry/systemctl-%EC%82%AC%EC%9A%A9%EB%B2%95?category=564154) [Get your Dream]
