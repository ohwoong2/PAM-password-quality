# PAM-password-quality
PAM을 사용해서 패스워드 최소 글자 수를 8자로 설정

## PAM이란?
PAM(Pluggable Authentication Modules)은 리눅스 시스템에서 사용자 인증을 제어하는 모듈로, 각 응용 프로그램이 자체적으로 인증 로직을 구현할 필요 없이 PAM에 요청하여 인증을 수행한다. 

이를 통해 응용 프로그램은 시스템 파일에 직접 접근하지 않아 보안이 강화되며, 관리자는 인증 방식을 중앙에서 제어할 수 있다. 

## 인증 모듈 설치
```
$ sudo apt-get install libpam-pwquality
```

## password quality 담당 파일 설정
```
$ sudo vi /etc/pam.d/common-password
password        requisite                       pam_pwquality.so retry=3 minlen=8 enforce_for_root
```
<img src="https://github.com/user-attachments/assets/17b39515-0233-43f3-acc9-1cdd69a9f522">


## 설정 확인
<img src="https://github.com/user-attachments/assets/98e84067-ed03-43ce-a51b-943a818d2ef9">
