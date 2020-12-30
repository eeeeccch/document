# apt 주소 변경 (해외 -> 국내)
```bash
# apt 저장소 서버 주소를 국내로 변경함으로 쾌적하게 사용할 수 있음
> sudo vi /etc/apt/sources.list

:%s/archive.ubuntu.com/ftp.daum.net/g
:%s/security.ubuntu.com/ftp.daum.net/g
:wq!

# apt 저장소 업데이트
> sudo apt-get update
> sudo apt full-upgrade
```

# install nodejs & npm
```bash
# 방법 1. apt를 활용한 nodejs & npm 설치
sudo apt install nodejs npm
```

```bash
# 방법 2. NVM(Node Version Manager) 활용하여 설치
# 사용자 계정에 nvm 스크립트를 설치 
# 이 파일을 사용하려면 먼저 .bashrc 파일을 원본으로 지정
> curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
> source ~/.bashrc

# 설치 가능한 버전 확인
> nvm list-remote

# 원하는 버전 설치
> nvm install v14.15.3
```
