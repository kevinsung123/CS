
### ethernet 장치명 확인
```#nmcli d ```
	1. ```#vi /etc/sysconfig/network-scripts/ifcfg-enp3s0```
		- BOOTPROTO=static
### DNS설정
- nslookup : 네임서버 확인
- [enter link description here](https://jw3461.tistory.com/8)

### centos 덮개 덮어도 유지

- ``` #vi /etc/systemd/logind.conf```
- HandleLidSwithc=suspend(->ignore 수정)
- #systemctl restart systemd-logind 

### RHEL/Centos7 systemctl 사용법
- Target  관리
	1. target은 기존 SysVinit의 run level과 같은개념
	2. systemd 기본타겟명은 default.tar
