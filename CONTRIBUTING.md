# 🤝 리눅스 스터디 기여 가이드

> 이 문서는 스터디 레포에 처음 참여하는 팀원을 위한 단계별 안내서입니다.
> **Git을 처음 써보는 분도 이 문서만 따라오면 첫 기여까지 완료할 수 있어요!**
> 먼저 [week0/README.md](week0/README.md)를 읽고 이번 주차 구조를 확인하세요.
> Git 첫 제출은 [week0/session1.md](week0/session1.md)부터 시작하는 것을 권장합니다.

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
> Git 관련 상세 실습은 [week0/session1.md](week0/session1.md), [week0/session2.md](week0/session2.md)를 먼저 따라오세요.
> 이 문서에서는 공통 흐름만 짧게 정리합니다.

### 4-1. 시작 순서

1. [week0/README.md](week0/README.md)로 전체 일정을 확인합니다.
2. 첫 Git 제출은 [week0/session1.md](week0/session1.md)부터 진행합니다.
3. 그 다음 [week0/session2.md](week0/session2.md)로 브랜치와 PR 흐름을 이어갑니다.

### 4-2. 공통 흐름

1. 각자 clone한 `linux-study` 폴더를 VSCode로 엽니다.
2. 터미널에서 브랜치를 만듭니다.
3. `members/<아이디>/...md` 파일을 작성합니다.
4. `git add -> git commit -> git push`를 실행합니다.
5. GitHub에서 PR을 생성합니다.

### 4-3. 꼭 기억할 규칙

- `main`에서 직접 작업하지 않습니다.
- 브랜치는 `study/<아이디>-sessionN` 규칙을 사용합니다.
- 파일은 `members/<아이디>/` 아래에 올립니다.
- 자세한 명령어와 제출 예시는 `week0/session1.md`와 `week0/session2.md`를 기준으로 봅니다.

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
