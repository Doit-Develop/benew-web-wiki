# [AWS] EC2에 개인 유저 생성하기

## 정책
⚠ 최초 개인 유저 생성을 위한 경우를 제외하고 `ec2-user` 혹은 `root`로 로그인하여 ec2에 접속하지 않는다.

## 작업 방법
1. 터미널을 켜고 ssh를 이용하여 ec2에 접속한다. ([🔗 ssh로 EC2 접속하기](aws-access-ec2-with-ssh.md))

2. 유저를 생성하고, 패스워드를 설정한다.
```terminal
$ sudo adduser <username>
$ passwd <username>
```

3. 생성한 유저를 그룹에 추가한다.
```terminal
$ sudo usermod -aG wheel <username>
```

4. ssh 클라이언트를 종료하고 생성한 유저 이름으로 다시 접속을 해서 공용폴더인 `shared`에 접근이 되는지 확인한다.
```terminal
$ exit

$ ssh <username>@인스턴스의 탄력적 IP
```



