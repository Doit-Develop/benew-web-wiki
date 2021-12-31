# [AWS] RDS에 연결하기
1. (선택사항) MySQl Workbench, HeidiSQL 등 선호하는 프로그램을 설치한다. 터미널 베이스가 편하면 MySQL Client를 사용해도 된다.

> UI 지원하는 프로그램 중에 고민이라면 ERD 생성 등 다양한 기능을 지원하는 MySQL Workbench 추천👍, 가볍운 HeidiSQL 추천👍

2. AWS RDS 보안그룹에 본인의 IP를 추가 혹은 업데이트한다.
▶ RDS > 연결&보안 > VPC 보안그룹 > 인바운드 규칙 편집

3. RDS의 **엔드포인트 IP**와 **포트**를 확인한다.
▶ RDS > 데이터베이스 > 해당 데이터베이스 선택 > 연결&보안 탭에서 엔드포인트와 포트 확인

4. 설치한 데이터베이스 관리 프로그램을 실행하고 다음의 정보로 새로운 세션을 추가한다.
네트워크 유형: MySQL(TCP/IP)
호스트명/IP: RDS 엔드포인트
포트: RDS 포트
사용자명: Benew 공용계정정보 확인
비밀번호: Benew 공용계정정보 확인

- MySQL Client를 사용한다면 다음 명령어로 접속한다.
```terminal
mysql -u <Benew 공용계정 사용자명> -p <RDS 포트> -h <RDS 엔드포인트>
```

