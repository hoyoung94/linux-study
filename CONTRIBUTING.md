# 🤝 리눅스 스터디 기여 가이드

> 이 문서는 스터디 레포에 처음 참여하는 팀원을 위한 단계별 안내서입니다.
> **Git을 처음 써보는 분도 이 문서만 따라오면 첫 기여까지 완료할 수 있어요!**
> 먼저 [week0/README.md](week0/README.md)를 읽고 이번 주차 과제 구조를 확인한 뒤 진행하세요.

---

## 📌 목차

1. [사전 준비](#1-사전-준비)
2. [Git과 GitHub 개념 이해](#2-git과-github-개념-이해)
3. [레포 초대 수락](#3-레포-초대-수락)
4. [첫 기여 실습](#4-첫-기여-실습)
5. [규칙 & 참고사항](#5-규칙--참고사항)

---

## 1. 사전 준비

### 1-1. Git 설치 (Windows)

**① 아래 링크에서 Git 설치 파일 다운로드**

👉 https://git-scm.com/download/win

- 사이트에 들어가면 자동으로 다운로드가 시작돼요
- 파일명이 `Git-x.xx.x-64-bit.exe` 형태면 정상

**② 설치 파일 실행**

설치 중 옵션이 많이 나오는데 **전부 기본값(Next)으로 진행하세요.**
딱 하나만 확인:

```
Choosing the default editor used by Git
→ "Use Visual Studio Code as Git's default editor" 선택 (VS Code 있는 경우)
→ VS Code 없으면 그냥 기본값(Vim)으로 Next
```

**③ 설치 완료 확인**

설치가 끝나면 **Windows 검색창**에 `Git Bash` 검색 → 실행

아래 명령어 입력:
```bash
git --version
```

이렇게 뜨면 설치 성공! ✅
```
git version 2.xx.x.windows.x
```

---

### 1-2. Git 초기 설정

Git Bash를 열고 아래 명령어를 **한 줄씩** 입력하세요.

> ⚠️ 이메일은 반드시 **GitHub 가입 이메일**과 동일해야 해요!
> 다르면 커밋이 본인 기여로 인정되지 않아요.

```bash
git config --global user.name "본인이름"
```
```bash
git config --global user.email "GitHub가입이메일@example.com"
```

**설정 확인:**
```bash
git config --global user.name
git config --global user.email
```

본인 이름과 이메일이 출력되면 성공! ✅

---

### 1-3. PAT (Personal Access Token) 발급

> PAT는 GitHub에 푸시할 때 비밀번호 대신 사용하는 토큰이에요.

**① GitHub 로그인 → 우측 상단 프로필 아이콘 클릭 → Settings**

**② 왼쪽 맨 아래 `Developer settings` 클릭**

**③ `Personal access tokens` → `Tokens (classic)` 클릭**

**④ `Generate new token` → `Generate new token (classic)` 클릭**

**⑤ 아래와 같이 설정:**

| 항목 | 설정값 |
| --- | --- |
| Note | `내 노트북용` |
| Expiration | `90 days` |
| Scopes | `repo` 전체 체크 ✅, `workflow` 체크 ✅ |

**⑥ 맨 아래 `Generate token` 클릭**

**⑦ 생성된 토큰 복사 후 메모장에 저장**

> ⚠️ **지금 복사 안 하면 다시 볼 수 없어요!**
> 창 닫기 전에 반드시 메모장에 붙여넣기 해두세요.

토큰 형태: `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxx`

---

## 2. Git과 GitHub 개념 이해

### Git vs GitHub

| 구분 | 설명 | 비유 |
| --- | --- | --- |
| **Git** | 내 컴퓨터에서 버전을 관리하는 도구 | 개인 일기장 |
| **GitHub** | Git 저장소를 인터넷에 올려 팀과 공유하는 플랫폼 | 공유 구글 드라이브 |

### 브랜치(Branch)란?

> 메인 코드를 건드리지 않고 **내 작업 공간을 따로 만드는 것**

```
main ─────────────────────────────▶ (팀 공용 공간, 보호됨 🔒)
         │
         └─── study/내아이디-session1 ──▶ (내 작업 공간 ✅)
```

### PR(Pull Request)란?

> "**내 브랜치의 작업을 main에 합쳐주세요!**" 라고 요청하는 것

```
내 브랜치에서 작업
      ↓
PR 생성 (합쳐달라고 요청)
      ↓
Merge (main에 반영)
      ↓
내 브랜치 삭제 (역할 끝)
```

### 우리 팀 협업 흐름

```
1. 새 브랜치 생성 (study/내아이디-sessionN)
2. 브랜치에서 파일 작성
3. 커밋 (저장)
4. PR 생성
5. Merge
6. 브랜치 삭제
```

---

## 3. 레포 초대 수락

> 스터디장이 GitHub 이메일로 초대를 보냈어요. 아래 순서로 수락하세요.

**① 가입한 이메일 메일함 확인**

- 발신: `noreply@github.com`
- 제목: `You've been invited to collaborate on hoyoung94/linux-study`
- 스팸함도 꼭 확인!

**② 메일 안의 `View invitation` 버튼 클릭**

**③ GitHub 로그인 상태에서 `Accept invitation` 클릭**

**④ 수락 완료 확인**

아래 URL 접속했을 때 레포가 보이면 성공! ✅
```
https://github.com/hoyoung94/linux-study
```

> ⚠️ 메일을 못 받았다면?
> 스터디장에게 GitHub 아이디 알려주고 재초대 요청하세요.

---

## 4. 첫 기여 실습

> **핵심 파트예요!** 천천히 따라오세요.
> 문서 작성은 **VSCode**, Git 명령은 **터미널**, 최종 제출은 **GitHub PR**로 진행합니다.

### 4-1. 로컬에 레포 준비

처음 하는 사람은 작업할 폴더에서 아래 명령어를 입력하세요.

```bash
cd C:\Users\HP\Documents\프로젝트\진행중
git clone https://github.com/hoyoung94/linux-study.git
cd linux-study
```

이미 `linux-study`를 clone한 상태라면 VSCode에서 그 폴더를 열고, `터미널 -> 새 터미널`만 열면 됩니다.

### 4-2. `main` 최신화

```bash
git switch main
git pull origin main
```

### 4-3. 작업 브랜치 만들기

아래 명령어로 이번 과제용 브랜치를 만듭니다.

```bash
git switch -c study/본인아이디-session1
```

예:

```bash
git switch -c study/kimjihoon-session1
```

> `git switch`가 안 되면 `git checkout -b study/본인아이디-session1`으로 실행해도 됩니다.

### 4-4. 새 파일 만들기

VSCode 탐색기에서 아래 경로로 파일을 만듭니다.

```
members/본인GitHub아이디/2026-04-24-git-session1.md
```

예:

- GitHub 아이디가 `kimjihoon`이면 `members/kimjihoon/2026-04-24-git-session1.md`

아래 템플릿을 그대로 붙여넣고 저장합니다.

```markdown
# Git 기초 학습 Session 1 (2026-04-24)

## 오늘 배운 개념
- 

## 오늘 실습한 명령어
- `git status`
- `git add`
- `git commit`
- `git push`

## 직접 해본 것
- 

## 헷갈렸던 점
- 

## 다음 학습 예정
- 
```

### 4-5. 상태 확인 + add

터미널에서 아래 명령어를 입력합니다.

```bash
git status
git add members/본인GitHub아이디/2026-04-24-git-session1.md
git status
```

첫 번째 `git status`에서는 새 파일이 보이고, `git add` 뒤에는 커밋할 파일로 올라간 상태가 보이면 정상입니다.

### 4-6. commit 만들기

```bash
git commit -m "docs: [git-session1] Git 기초와 첫 업로드"
```

### 4-7. GitHub로 push

```bash
git push -u origin study/본인아이디-session1
```

예:

```bash
git push -u origin study/kimjihoon-session1
```

> push 과정에서 로그인 창이 뜨면 GitHub 비밀번호 대신 PAT를 입력합니다.

### 4-8. Pull Request 생성

1. GitHub에서 `https://github.com/hoyoung94/linux-study`를 엽니다.
2. `Compare & pull request` 버튼이 보이면 클릭합니다.
3. 버튼이 안 보이면 `Pull requests -> New pull request`로 들어갑니다.
4. 제목을 아래처럼 적습니다.

```
docs: [git-session1] Git 기초와 첫 업로드
```

5. 본문은 아래 예시를 참고해서 적습니다.

```markdown
## 변경 내용
- `members/본인아이디/2026-04-24-git-session1.md` 추가
- Session 1 Git 기초 실습 기록 정리

## 체크리스트
- [x] 로컬에서 `git add`, `git commit`, `git push`를 실행함
- [x] 브랜치 규칙을 지킴
```

6. `Create pull request`를 누릅니다.

### 4-9. Merge

PR 승인 후에는 아래 순서로 머지합니다.

1. `Merge pull request` 클릭
2. `Confirm merge` 클릭

### 4-10. 브랜치 삭제

머지 후에는 GitHub에서 `Delete branch`를 눌러 정리합니다.

### 4-11. 완료 확인 ✅

아래 URL에서 본인 폴더가 보이면 성공! 🎉
```
https://github.com/hoyoung94/linux-study/tree/main/members/본인아이디
```

---

## 5. 규칙 & 참고사항

### 커밋 메시지 규칙

```
docs: [주제] 내용 요약

예시:
docs: [git-session1] Git 기초와 첫 업로드
docs: [git-session2] 브랜치와 PR 실습
docs: [week1] 파일 시스템 정리
study: [week2] 권한 관리 실습 기록
```

| prefix | 사용 상황 |
| --- | --- |
| `docs:` | 문서 추가·수정 |
| `study:` | 학습 기록·실습 결과 |

### 파일명 규칙

```
YYYY-MM-DD-주제.md

예시:
2026-04-24-git-session1.md
2026-04-26-git-session2.md
2026-04-28-shell-script.md
```

### 브랜치 이름 규칙

```
study/본인아이디-sessionN

예시:
study/kimjihoon-session1
study/kimjihoon-session2
```

### ⚠️ 자주 하는 실수

| 실수 | 해결 방법 |
| --- | --- |
| `git switch -c`가 안 돼요 | `git checkout -b 브랜치이름`으로 대신 실행 |
| `git push`에서 인증이 막혀요 | GitHub 비밀번호 대신 PAT를 입력 |
| 초대 메일을 못 받았어요 | 스팸함 확인 후 스터디장에게 재초대 요청 |
| PAT 토큰을 복사 안 했어요 | Settings에서 새 토큰 다시 발급 |
| 브랜치 삭제를 깜빡했어요 | 레포 → branches → 해당 브랜치 옆 🗑️ 클릭 |
| 파일명을 한글로 썼어요 | 영문+숫자+하이픈만 사용 |

### 막혔을 때

> 이 문서 봐도 모르겠으면 스터디 단톡방에 **스크린샷과 함께** 올려주세요!
> 혼자 30분 이상 고민하지 마세요. 바로 물어보는 게 팀 전체에 도움이 돼요. 🙂

---

*last updated: 2026-04-23*
