# Session 2: 브랜치와 PR 실습

> 이번 세션의 목표는 `main`을 최신화하고, 새 브랜치를 만든 뒤, 로컬에서 커밋과 push를 해서 PR까지 올려보는 것입니다.
> 오늘 할 일은 1. `linux-study` 폴더 다시 열기 2. VSCode에서 문서 작성 3. 터미널에서 브랜치와 push 실습 4. GitHub에서 PR 생성 입니다.

## 0. 시작 전에 확인

이 문서는 **Session 1을 끝낸 뒤 이어서 진행하는 문서**입니다.

- 이미 내 컴퓨터에 `linux-study` 저장소가 clone되어 있다고 가정합니다.
- 여기서 말하는 `linux-study` 폴더는 각자 자기 컴퓨터에 clone한 폴더입니다.
- 사람마다 저장 위치는 다를 수 있습니다.
- 새 빈 폴더를 만들라는 뜻이 아닙니다.

먼저 확인할 것:

1. Session 1에서 사용한 `linux-study` 폴더가 내 컴퓨터에 있는지
2. 그 폴더를 VSCode에서 다시 열었는지
3. Git Bash 또는 VSCode 터미널을 열 수 있는지

만약 아직 `linux-study`가 없거나 Session 1을 하지 않았다면:

- 먼저 [session1.md](./session1.md)를 보고 `git clone`부터 진행합니다.
- Session 2는 Session 1이 끝난 뒤 시작하는 것이 맞습니다.

## 1. 이번 세션에서 할 일

1. Session 1에서 사용한 `linux-study` 폴더를 VSCode로 다시 엽니다.
2. `main`을 최신 상태로 맞춥니다.
3. 새 브랜치 `study/<아이디>-session2`를 만듭니다.
4. 문서를 작성하고 `git add`, `git commit`, `git push`를 실행합니다.
5. GitHub에서 PR을 생성합니다.

## 2. 무엇을 제출하나요?

제출물은 아래 3개입니다.

- Markdown 파일 1개
- 브랜치 1개
- PR 1개

제출 파일 경로:

```text
members/<본인GitHub아이디>/2026-04-26-git-session2.md
```

브랜치 이름:

```text
study/<아이디>-session2
```

PR 제목:

```text
docs: [git-session2] 브랜치와 PR 실습
```

## 3. 어디에서 문서를 작성하나요?

문서는 **VSCode에서 작성**합니다.

여기서 말하는 `linux-study` 폴더는 Session 1 때 사용했던 저장소 폴더입니다.  
절대경로는 사람마다 다르므로 문서에서는 고정 경로를 쓰지 않습니다.

순서:

1. VSCode에서 `linux-study` 폴더를 엽니다.
2. `members/<본인GitHub아이디>/` 폴더 안에 `2026-04-26-git-session2.md` 파일을 만듭니다.
3. 아래 템플릿을 붙여넣고 내용을 채운 뒤 저장합니다.

`.md` 파일은 메모장처럼 글을 적는 텍스트 문서라고 생각하면 됩니다.

## 4. 명령어 친 내용은 어떻게 적나요?

터미널 화면 전체를 제출하는 것이 아닙니다.  
문서에 아래 3가지만 적으면 됩니다.

- 내가 입력한 명령어
- 화면에 나온 핵심 결과
- 내가 이해한 한 줄

예를 들면 아래처럼 적으면 됩니다.

````md
## 오늘 실습한 명령어

```bash
git switch main
git pull origin main
```

## 실행 결과

```text
Already on 'main'
Already up to date.
```

## 내가 이해한 것

- `git switch main`은 main 브랜치로 이동하는 명령어다.
- `git pull origin main`은 최신 main 내용을 내 컴퓨터로 가져오는 명령어다.
````

## 5. 실습 순서

### 5-1. `linux-study` 폴더 다시 열기

Session 1 때 사용했던 같은 `linux-study` 폴더를 VSCode에서 다시 엽니다.

아직 이 폴더가 없다면 Session 2를 바로 시작하지 말고, 먼저 [session1.md](./session1.md)를 따라 `git clone`부터 진행합니다.

그 다음 VSCode 상단 메뉴에서 `터미널 -> 새 터미널`을 누릅니다.

### 5-2. `main` 최신화

터미널에서 아래 명령어를 순서대로 입력합니다.

```bash
git switch main
git pull origin main
```

문서에는 아래를 적습니다.

- `main`으로 이동했는지
- `pull` 결과가 어땠는지
- `git pull`이 무엇을 하는지 한 줄 설명

### 5-3. 새 브랜치 만들기

이제 이번 과제용 브랜치를 만듭니다.

```bash
git switch -c study/<아이디>-session2
```

예:

```bash
git switch -c study/hoyoung94-session2
```

> `git switch`가 안 되면 `git checkout -b study/<아이디>-session2`로 실행해도 됩니다.

문서에는 아래를 적습니다.

- 어떤 브랜치를 만들었는지
- 왜 `main`이 아니라 새 브랜치에서 작업하는지

### 5-4. 제출 문서 만들기

아래 경로로 파일을 만들고 저장합니다.

```text
members/<본인GitHub아이디>/2026-04-26-git-session2.md
```

### 5-5. 상태 확인

```bash
git status
```

문서에는 아래를 적습니다.

- 새 파일이 보였는지
- 현재 브랜치가 무엇인지

### 5-6. `git add` 해보기

```bash
git add members/<본인GitHub아이디>/2026-04-26-git-session2.md
```

문서에는 아래를 적습니다.

- 입력한 명령어
- `git add` 뒤에 상태가 어떻게 바뀌었는지

### 5-7. `git commit` 해보기

```bash
git commit -m "docs: [git-session2] 브랜치와 PR 실습"
```

문서에는 아래를 적습니다.

- 입력한 명령어
- 화면에 나온 커밋 결과 한 줄

### 5-8. `git push` 해보기

```bash
git push -u origin study/<아이디>-session2
```

예:

```bash
git push -u origin study/hoyoung94-session2
```

문서에는 아래를 적습니다.

- 입력한 명령어
- 화면에 나온 핵심 결과
- 로컬 브랜치와 GitHub 브랜치가 연결됐는지

### 5-9. GitHub에서 PR 만들기

1. GitHub에서 `linux-study` 저장소를 엽니다.
2. `Compare & pull request`를 누릅니다.
3. PR 제목을 아래처럼 적습니다.

```text
docs: [git-session2] 브랜치와 PR 실습
```

4. PR을 생성합니다.

문서에는 아래를 적습니다.

- 브랜치가 왜 필요한지
- PR이 어떤 역할을 하는지

## 6. 제출 문서 템플릿

아래 템플릿을 그대로 복붙해서 작성하면 됩니다.

````md
# Git 기초 학습 Session 2 (2026-04-26)

## 오늘 배운 개념
- `git pull`은 원격 저장소의 최신 내용을 내 컴퓨터로 가져오는 명령어다.
- 브랜치는 main을 직접 건드리지 않고 따로 작업하는 공간이다.
- `git push`는 내 브랜치의 커밋을 GitHub에 올리는 단계다.
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
Already on 'main'
Already up to date.
Switched to a new branch 'study/hoyoung94-session2'
[study/hoyoung94-session2 abc1234] docs: [git-session2] 브랜치와 PR 실습
branch 'study/hoyoung94-session2' set up to track 'origin/study/hoyoung94-session2'
```

## 직접 해본 것
- `main`을 최신 상태로 맞췄다.
- 새 브랜치를 만들어 그 안에서 작업했다.
- 로컬에서 커밋한 뒤 GitHub에 push했다.
- PR을 생성했다.

## 헷갈렸던 점
- `main`에서 바로 작업하면 안 되는 이유를 더 익히고 싶다.

## 이제 혼자 할 수 있는 것
- `git pull`로 최신 내용을 받아올 수 있다.
- 새 브랜치를 만들 수 있다.
- 커밋한 내용을 GitHub에 push할 수 있다.
- PR이 어떤 역할을 하는지 설명할 수 있다.
````

## 7. 제출 방법

1. VSCode에서 문서를 작성하고 저장합니다.
2. 터미널에서 `git switch main -> git pull -> git switch -c -> git add -> git commit -> git push` 순서로 진행합니다.
3. GitHub에서 PR을 생성합니다.
4. 화면이 헷갈리면 [CONTRIBUTING.md](../CONTRIBUTING.md)를 같이 봅니다.

## 8. 완료 기준

- [ ] `members/<본인GitHub아이디>/2026-04-26-git-session2.md` 파일을 만들었다.
- [ ] `git switch main`과 `git pull origin main`을 실행했다.
- [ ] `git switch -c study/<아이디>-session2` 또는 `git checkout -b ...`를 실행했다.
- [ ] `git status`를 실행했다.
- [ ] `git add`를 실행했다.
- [ ] `git commit`을 실행했다.
- [ ] `git push`를 실행했다.
- [ ] 브랜치와 PR의 역할을 문장으로 적었다.
- [ ] 실습 내용을 `.md` 문서에 정리했다.
- [ ] `study/<아이디>-session2` 브랜치가 GitHub에 올라갔다.
- [ ] PR을 생성했다.
