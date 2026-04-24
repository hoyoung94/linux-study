# Git 기초 학습 Session 2 (2026-04-26)

## 오늘 배운 개념
- `git pull`은 GitHub의 최신 내용을 내 컴퓨터로 가져오는 명령어다.
- 브랜치는 main을 직접 건드리지 않고 따로 작업하는 공간이다.
- PR은 내 브랜치 작업을 main에 합쳐달라고 요청하는 단계다.

## 오늘 실습한 명령어

```bash
git switch main
git pull origin main
git switch -c study/hoyoung94-session2
git status
git add members/hoyoung94/2026-04-26-git-session2.md
git commit -m "docs: [git-session2] 브랜치와 PR 실습"
git push -u origin study/hoyoung94-session2
```

## 실행 결과

```text
Already up to date.
Switched to a new branch 'study/hoyoung94-session2'
[study/hoyoung94-session2 abc1234] docs: [git-session2] 브랜치와 PR 실습
branch 'study/hoyoung94-session2' set up to track 'origin/study/hoyoung94-session2'
```

## 직접 해본 것
- `git pull`로 main을 최신화했다.
- 새 브랜치를 만들어 그 안에서 작업했다.
- 로컬에서 커밋한 뒤 GitHub에 push했다.
- PR을 생성했다.

## 헷갈렸던 점
- `git pull`을 안 하고 브랜치를 따면 어떻게 되는지 궁금하다.
 - 브랜치를 삭제를 로컬이랑 서버랑 둘다해야해요 나 할수있어요!

## 다음 학습 예정
- 다음 세션에서 충돌 해결과 merge 흐름을 익힐 예정이다.

수정합니다악