# PAM-password-quality

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
