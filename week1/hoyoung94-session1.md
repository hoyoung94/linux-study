# week1 session1: 실습 환경 준비 & 파일·디렉토리 다루기

## 오늘 배운 것
-내 가상머신 IP 주소는 
ens33:
inet 192.168.100.138/24
/var/log/syslog가 없는 환경도 있다.
내 VM은 syslog 파일 대신 systemd journal 로그를 사용한다.
실시간 로그 확인은 journalctl -f로 할 수 있다.

## 실습한 명령어

```bash
# 디렉토리 이동
cd /tmp
cd ..
cd ~
cd /var/log

# 중간 경로까지 한 번에 생성
mkdir -p project/src/api

# 상위 디렉토리의 다른 폴더로 복사
cp note.txt ../day2/
cp note.txt ../day3/

# 한 줄로 여러 명령 실행
cp note.txt ../day2/ && cp note.txt ../day3/
```

## 헷갈렸던 점
-
mkdir project/src/api     # 실패 가능
mkdir -p project/src/api  # 맞음
- 
경로 관련 실수
cp note.txt study/day2 study/day3   # 틀림
cp note.txt ../day2/                # 맞음
cp note.txt ../day3/                # 맞음

## 다음에 복습할 것
-
절대경로와 상대경로 차이
., .., ~, / 의미
cp, mv, rm, mkdir -p 사용법
head, tail, less, cat 차이
journalctl을 이용한 로그 확인
SSH 접속 로그 확인 방법