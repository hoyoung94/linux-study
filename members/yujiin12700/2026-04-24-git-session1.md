# Git 기초 학습 Session 1 (2026-04-24)

## git add
명령어 : git add members/yujiin12700/2026-04-24-git-session1.md
결과 : git add 를 입력하니까 untracked files 였던게 commit할 준비가 된 상태로 바뀌었다
한줄 정리 : git add는 commit할 파일을 선택해서 올려두는 것

## git switch
명령어 : git switch -c study/yujiin12700-session1
결과 : Switched to a new branch 'study/yujiin12700-session1'
한줄 정리 : git switch -c 새 브랜치 만들고 브랜치로 이동. (-c : create)

## git status
git add 전 상태
Untracked files:
  (use "git add <file>..." to include in what will be committed)
git add 한 뒤
On branch study/yujiin12700-session1
Changes to be committed:                                           
  (use "git restore --staged <file>..." to unstage)      
        new file:   members/yujiin12700/2026-04-24-git-session1.md

## git commit
명령어 : git commit -m "docs: [git-session1] Git 기초와 첫 업로드"
결과 : nothing to commit, working tree clean
한줄 정리 : git commit은 변경사항을 하나의 기록으로 저장하는 것

## git push
명령어 : git push -u origin study/yujiin12700-session1
결과 : branch 'study/yujiin12700-session1' set up to track 'origin/study/yujiin12700-session1'.
한줄 정리 : git push는 내 컴퓨터에 있는 커밋을 Github 같은 원격 저장소로 업로드 하는 것


## 직접 해본 것
- `git switch`로 새 브랜치를 만들었다.
- `git add`로 파일을 스테이징했다.
- `git commit`으로 기록을 남겼다.
- `git push`로 GitHub에 올렸다.

## 헷갈렸던 점
- vs코드에서 파일을 여는 방법을 몰랐다 .ㅎㅎ 다른건 설명대로 따라하니 쉬웠음!

## 다음 학습 예정
- 다음 세션에서 `git pull`, 브랜치, PR 흐름을 더 익힐 예정이다.
