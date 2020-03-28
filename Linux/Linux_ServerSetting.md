### 서버 구축 

1. centos7 부팅 usb 준비 
	- centos7 iso이미지 다운로드  [enter link description here](https://www.centos.org/download/)
	- Rufus를 이용한 부팅USB준비
	- centos7 설치 [enter link description here](http://blog.naver.com/anysecure3/221571814401)
		- 설치대상 : centos7 설치할 디스크를 선택하고 파티셔닝
		- 네트워크 및 호스트명 
			- centos 네트워크 카드확인
				1. ``` #nmcli d ```
				2. ``` #ip addr ```
				3. ``` #ifconfig -a ```
			- 이더넷(eth0)
				- ip addr 이후 나오는 네트워크인터페이스명 확인(무선/유선)
				- ``` #yum install net-tools```(network패키지 설치)
				- ``` #yum -y install bind-utils wget elinks vim```(vim 및 network 관려유틸)
				- ```yum -y install yum-utils sysstat system-config-firewall-tui ```
				- ```yum -y install man man-pages kernel-doc ```
				1.  서버에서 도메인을 제일 먼저 찾는곳
				- #vi /etc/hosts
				2. 서버에서 사용할 DNS
				-  #vi /etc/resolv.conf
					```
					nameserver 192.168.1.100 
					nameserver 168.126.63.1
					nameserver 168.126.63.2 
					```
				3. 도메인대한 ip를 참조할때 순서
				- #vi /etc/host.conf
				4. 방화벽 확인 [enter link description here](https://conory.com/blog/42477)
			- 무선
				1. NetWorkManager이용
					- #yum -y install NetworkManager-wifi
					- #systemctl restart NetworkManager
					- #nmcli dev wifi list
					- #nmcli --ask dev wifi connect 와아파이이름
### ※ 서버 셋팅 Tip
#### .bashrc 와 .bash_profile 차이
[enter link description here](https://uroa.tistory.com/114)

#### history Timforamt 지정
- / etc/profile
	- export HISTTIMEFORMAT="[%F %T ]"
	> %F : full date
	> %T :  time same as %H:%M:%S
	> [시간포맷](https://www.cyberciti.biz/faq/linux-unix-formatting-dates-for-display/)
	- source /etc/profile
	- 
