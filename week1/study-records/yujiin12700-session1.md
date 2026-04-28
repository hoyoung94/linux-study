# week1 session1: 실습 환경 준비 & 파일·디렉토리 다루기

## 오늘 배운 것
- Ubuntu Server 설치
MobaXterm 실행해서 새 세션을 만들고 우분투 접속
파일과 디렉토리 만들기, 위치 확인과 이동, 복사, 삭제
여러 파일을 한번에 만들고 -p로 부모폴더 만들기!
sudo journalctl 로그확인
vm 스냅샷 찍기

## 실습한 명령어

```bash
echo "Hello, MobaXterm!"  # "Hello, MobaXterm!" 출력
lsb_release -a            # Ubuntu 버전
uname -a                  # 커널 정보
hostname                  # 호스트명
whoami                    # 현재
mkdir myapp               # 폴더 생성
touch test.txt            # 빈 파일
touch a.txt b.txt c.txt   # 여러 파일 한번에
pwd                       # 현재 위치
ls                        # 파일 목록
ls -l                     # 상세 정보
ls -la                    # 숨김 파일까지 (실무 표준)

cd /var/log               # 절대 경로 이동
cd ..                     # 상위 폴더
cd ~                      # 홈 디렉토리
cd $home
cp a.txt b.txt               # 파일 복사

mv old.txt new.txt           # 이름 변경
mv file.txt /tmp/            # 이동

rm test.txt                  # 파일 삭제
rm -rf folder/               # 폴더 강제 삭제
cat app.log              # 파일 내용 전체 출력
cat a.txt b.txt          # 여러 파일 이어서 출력
less app.log
head app.log             # 처음 10줄
head -n 20 app.log       # 처음 20줄
tail app.log             # 마지막 10줄
tail -n 50 app.log       # 마지막 50줄
tail -f app.log          # 실시간으로 따라가기 ⭐️
ls --help                # 간단한 도움말
man ls                   # 상세 매뉴얼 (q로 종료)
sudo journalctl -f       # 로그 모니터링

```

## 헷갈렸던 점
-파일을 복사해서 다른 위치에 있는 폴더에 넣을 때 상위에 위치한 폴더라서 ../day2 처럼 앞에 ../를 붙어야 했다
-cp a.txt b.txt  를 했을 때 원래 두개 파일이 모두 생성되어 있어서 a.txt파일이 b.txt라는 이름의 파일로 그대로 복사되는 것을 몰랐다. 
  b.txt를 지우고 다시 cp a.txt b.txt를 입력하니 b.txt파일이 생겨났다.

## 다음에 복습할 것
-파일을 복사할 때 파일 위치 잘 확인하기
-log 확인하기
