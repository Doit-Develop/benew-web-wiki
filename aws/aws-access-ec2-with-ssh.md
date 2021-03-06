# [AWS] ssh 클라이언트로 EC2에 접속하기

## 준비물
- 프라이빗 키 페어 파일(`pem` 파일)
- EC2 인스턴스의 `탄력적 IP` 혹은 `퍼블릭 IPv4 DNS`

## 작업 방법
1. 터미널을 켜고 키 페어 파일(`pem` 파일)이 위치한 디렉토리로 이동한다.

2. ssh 명렁어로 접속한다.
```terminal
$ ssh -i private_key.pem 사용자이름@인스턴스의 탄력적 IP
```
- 인스턴스의 `탄력적 IP` 대신 `퍼블릭 IPv4 DNS`를 입력해도 된다.

## 🚀 Trouble Shooting
*에러 발생 시 다음을 확인해보자!*
- [ ] EC2 보안그룹 인바운드에 나의 IP를 추가&최신 상태로 업데이트 했는지
- [ ] 유효한 키페어 파일을 가지고 있는지
- [ ] 키페어 파일이 있는 경로에서 접속을 시도했는지
