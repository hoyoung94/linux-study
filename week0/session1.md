# Session 1: Git 기초와 첫 업로드

> 이번 세션의 목표는 내 컴퓨터에서 `git add`, `git commit`, `git push`를 직접 해보고, 그 과정을 문서로 정리해 GitHub PR까지 올려보는 것입니다.
> 오늘 할 일은 1. `linux-study` 폴더 준비 2. VSCode에서 문서 작성 3. 터미널에서 Git 명령 실행 4. GitHub에서 PR 생성 입니다.

## 0. 시작 전에 확인

이 문서에서 말하는 `linux-study` 폴더는 **각자 자기 컴퓨터에 clone해 둔 저장소 폴더**를 뜻합니다.

- 바탕화면에 새 빈 폴더를 임의로 만들라는 뜻이 아닙니다.
- 경로는 사람마다 다를 수 있습니다.
- 중요한 것은 `git clone`으로 내려받은 `linux-study` 폴더를 여는 것입니다.

이미 `linux-study`를 clone했다면:

- 그 폴더를 VSCode에서 엽니다.

아직 `linux-study`가 없다면:

1. 원하는 작업 폴더를 정합니다.
예: 바탕화면, 문서, 프로젝트 폴더
2. 그 위치에서 아래 명령어를 실행합니다.

```bash
git clone https://github.com/hoyoung94/linux-study.git
```

3. 그러면 `linux-study` 폴더가 새로 생깁니다.
4. 그 생성된 `linux-study` 폴더를 VSCode에서 엽니다.

VSCode에서 여는 방법:

1. VSCode 실행
2. `파일 -> 폴더 열기`
3. 방금 clone한 `linux-study` 폴더 선택
4. 열기

> 핵심은 `새 폴더를 직접 만드는 것`이 아니라 `clone으로 생성된 linux-study 폴더를 여는 것`입니다.

## 1. 이번 세션에서 할 일

1. 내 컴퓨터에 clone된 `linux-study` 폴더를 VSCode로 엽니다.
2. 제출 문서 `2026-04-24-git-session1.md`를 만듭니다.
3. 터미널에서 `git add`, `git commit`, `git push`를 직접 실행합니다.
4. GitHub에서 PR을 생성합니다.

## 2. 무엇을 제출하나요?

제출물은 아래 3개입니다.

- Markdown 파일 1개
- 브랜치 1개
- PR 1개

제출 파일 경로:

```text
members/<본인GitHub아이디>/2026-04-24-git-session1.md
```

브랜치 이름:

```text
study/<아이디>-session1
```

PR 제목:

```text
docs: [git-session1] Git 기초와 첫 업로드
```

> 기본 제출물은 `.md` 문서입니다. 메모장처럼 글을 적는 텍스트 파일이라고 생각하면 됩니다.

## 3. 어디에서 문서를 작성하나요?

문서는 **VSCode에서 작성**합니다.

여기서 말하는 `linux-study` 폴더는 각자 자기 컴퓨터에 clone해 둔 폴더입니다.  
절대경로는 사람마다 다르므로 문서에서는 고정 경로를 쓰지 않습니다.

순서:

1. VSCode에서 `linux-study` 폴더를 엽니다.
2. `members/<본인GitHub아이디>/` 폴더가 없으면 새로 만듭니다.
3. 그 안에 `2026-04-24-git-session1.md` 파일을 만듭니다.
4. 아래 템플릿을 붙여넣고 내용을 채운 뒤 저장합니다.

## 4. 명령어 친 내용은 어떻게 적나요?

터미널 화면을 통째로 제출하는 것이 아닙니다.  
VSCode 문서 안에 아래 3가지만 적으면 됩니다.

- 내가 입력한 명령어
- 화면에 나온 핵심 결과
- 내가 이해한 한 줄

예를 들면 아래처럼 적으면 됩니다.

````md
## 오늘 실습한 명령어

```bash
git status
git add members/hoyoung94/2026-04-24-git-session1.md
```

## 실행 결과

```text
On branch study/hoyoung94-session1
Changes to be committed:
```

## 내가 이해한 것

- `git status`는 현재 변경 상태를 보여준다.
- `git add`는 커밋할 파일을 올려두는 단계다.
````

헷갈리면 뜻을 완벽하게 쓰려고 하기보다 **명령어 + 결과 한 줄 + 내 말 한 줄**만 적으면 충분합니다.

## 5. 실습 순서

### 5-1. `linux-study` 폴더 열기

이미 `linux-study`를 clone 했다면 그 폴더를 VSCode로 열고, 상단 메뉴에서 `터미널 -> 새 터미널`을 누릅니다.

아직 clone하지 않았다면 원하는 작업 폴더에서 아래 명령어를 실행합니다.

```bash
git clone https://github.com/hoyoung94/linux-study.git
```

그 다음 생성된 `linux-study` 폴더를 VSCode로 열면 됩니다.

### 5-2. 작업 브랜치 만들기

터미널에서 아래 명령어를 입력합니다.

```bash
git switch -c study/<아이디>-session1
```

예:

```bash
git switch -c study/hoyoung94-session1
```

> `git switch`가 안 되면 `git checkout -b study/<아이디>-session1`으로 실행해도 됩니다.

### 5-3. 제출 문서 만들기

VSCode에서 아래 경로로 파일을 만듭니다.

```text
members/<본인GitHub아이디>/2026-04-24-git-session1.md
```

파일을 저장한 뒤 터미널로 돌아옵니다.

### 5-4. 상태 확인

```bash
git status
```

문서에는 아래를 적습니다.

- 내가 만든 파일이 보였는지
- `untracked files` 또는 `changes not staged` 같은 문구가 나왔는지
- `git status`가 무엇을 확인하는 명령어인지

### 5-5. `git add` 해보기

```bash
git add members/<본인GitHub아이디>/2026-04-24-git-session1.md
```

문서에는 아래를 적습니다.

- 입력한 `git add` 명령어
- `git add`를 한 뒤 다시 `git status`를 쳤을 때 무엇이 달라졌는지
- `git add`가 무엇을 하는지 한 줄 설명

### 5-6. `git commit` 해보기

```bash
git commit -m "docs: [git-session1] Git 기초와 첫 업로드"
```

문서에는 아래를 적습니다.

- 입력한 `git commit` 명령어
- 화면에 나온 커밋 결과 한 줄
- `git commit`이 무엇을 하는지 한 줄 설명

### 5-7. `git push` 해보기

```bash
git push -u origin study/<아이디>-session1
```

예:

```bash
git push -u origin study/hoyoung94-session1
```

문서에는 아래를 적습니다.

- 입력한 `git push` 명령어
- 화면에 나온 핵심 결과 한 줄
- `git push`가 무엇을 하는지 한 줄 설명

> 처음 push할 때 로그인이나 토큰 입력이 필요할 수 있습니다. GitHub 비밀번호 대신 PAT를 사용합니다.

### 5-8. GitHub에서 PR 만들기

1. GitHub에서 `linux-study` 저장소를 엽니다.
2. `Compare & pull request` 버튼이 보이면 클릭합니다.
3. 보이지 않으면 `Pull requests -> New pull request`로 들어갑니다.
4. PR 제목을 아래처럼 적습니다.

```text
docs: [git-session1] Git 기초와 첫 업로드
```

5. PR을 생성합니다.

## 6. 제출 문서 템플릿

아래 템플릿을 그대로 복붙해서 작성하면 됩니다.

````md
# Git 기초 학습 Session 1 (2026-04-24)

## 오늘 배운 개념
- `git add`는 커밋할 파일을 올려두는 단계다.
- `git commit`은 변경 내용을 하나의 기록으로 남기는 단계다.
- `git push`는 내 컴퓨터의 커밋을 GitHub에 올리는 단계다.

## 오늘 실습한 명령어

```bash
git switch -c study/hoyoung94-session1
git status
git add members/hoyoung94/2026-04-24-git-session1.md
git commit -m "docs: [git-session1] Git 기초와 첫 업로드"
git push -u origin study/hoyoung94-session1
```

## 실행 결과

```text
Switched to a new branch 'study/hoyoung94-session1'
Changes to be committed:
[study/hoyoung94-session1 abc1234] docs: [git-session1] Git 기초와 첫 업로드
branch 'study/hoyoung94-session1' set up to track 'origin/study/hoyoung94-session1'
```

## 직접 해본 것
- 새 브랜치를 만들었다.
- `git add`로 파일을 스테이징했다.
- `git commit`으로 기록을 남겼다.
- `git push`로 GitHub에 올렸다.

## 헷갈렸던 점
- `git add`와 `git commit`이 바로 이어지는 줄 알았는데 단계가 나뉘어 있었다.

## 다음 학습 예정
- 다음 세션에서 `git pull`, 브랜치, PR 흐름을 더 익힐 예정이다.
````

## 7. 제출 방법

1. VSCode에서 문서를 작성하고 저장합니다.
2. 터미널에서 `git add`, `git commit`, `git push`를 순서대로 실행합니다.
3. GitHub에서 PR을 생성합니다.
4. 화면 위치가 헷갈리면 [CONTRIBUTING.md](../CONTRIBUTING.md)를 같이 봅니다.

## 8. 완료 기준

- [ ] `members/<본인GitHub아이디>/2026-04-24-git-session1.md` 파일을 만들었다.
- [ ] `git switch -c study/<아이디>-session1` 또는 `git checkout -b ...`를 실행했다.
- [ ] `git status`를 실행해 현재 상태를 확인했다.
- [ ] `git add`를 실행했다.
- [ ] `git commit`을 실행했다.
- [ ] `git push`를 실행했다.
- [ ] 실습 내용을 `.md` 문서에 정리했다.
- [ ] `study/<아이디>-session1` 브랜치가 GitHub에 올라갔다.
- [ ] PR을 생성했다.
