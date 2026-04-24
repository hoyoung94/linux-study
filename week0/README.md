# week0: Git 기초와 첫 GitHub 업로드

> `week0`는 리눅스 스터디에 들어가기 전에 Git과 GitHub 협업 흐름을 먼저 익히는 공통 준비 주차입니다.

## 🎯 week0 목표

- Git과 GitHub의 차이를 이해한다.
- `add`, `commit`, `push` 흐름을 직접 한 번 해본다.
- 브랜치를 만들어 작업하고 PR로 제출하는 경험을 해본다.
- 충돌 해결, PR 리뷰, 실수 복구, 브랜치 전략까지 기본 협업 흐름을 정리한다.
- `git init`, `.gitignore`, `diff`, `log`로 커밋 전후 상태를 확인하는 기본기를 보강한다.

## 🗓️ 진행 일정

| 날짜 | 내용 | 문서 |
| --- | --- | --- |
| 2026-04-24 | Session 1: Git 기초와 첫 업로드 | [session1.md](./session1.md) |
| 2026-04-25 | 버퍼일: 복습 또는 미완료 과제 정리 | - |
| 2026-04-26 | Session 2: 브랜치와 PR 실습 | [session2.md](./session2.md) |
| 이후 진행 | Session 3: 충돌과 merge 해결 실습 | [session3.md](./session3.md) |
| 이후 진행 | Session 4: GitHub Flow와 PR 리뷰 워크플로우 | [session4.md](./session4.md) |
| 이후 진행 | Session 5: 실수 복구와 stash 실습 | [session5.md](./session5.md) |
| 이후 진행 | Session 6: 브랜치 전략과 협업 운영 정리 | [session6.md](./session6.md) |
| 이후 진행 | Session 7: Git 기본기 보강 - init, ignore, diff, log | [session7.md](./session7.md) |

> Session 1, 2는 기존 일정에 맞춰 진행하고, Session 3 이후는 필요에 따라 이어서 진행합니다.

## 📍 경로 기준

- 학습 문서: `week0/session1.md` ~ `week0/session7.md`
- 롤링페이퍼 충돌 실습 파일: `week0/conflict-practice/rolling-paper.md`
- 개인 제출 파일: 저장소 루트의 `members/<본인GitHub아이디>/` 아래에 작성
- 브랜치 규칙: `study/<아이디>-sessionN`

`week0/members/` 폴더는 만들지 않습니다.

## 🧭 Session 1-7 전체 흐름

| 세션 | 역할 | 이전 세션과의 연결 | 핵심 실습 |
| --- | --- | --- | --- |
| Session 1 | GitHub 제출 흐름 시작 | Git 저장소를 clone하고 첫 제출 흐름을 경험합니다. | `add`, `commit`, `push`, PR 생성 |
| Session 2 | 팀 협업 흐름으로 확장 | 개인 push 이후 `main` 최신화와 새 브랜치 작업을 익힙니다. | `pull`, 브랜치 생성, PR |
| Session 3 | 실제 충돌 재현과 해결 | 여러 PR이 같은 파일을 바꾸면 충돌이 생긴다는 점을 실습합니다. | `week0/conflict-practice/rolling-paper.md`, `merge main` |
| Session 4 | PR 품질과 리뷰 문화 | PR을 만드는 단계에서 잘 작성하고 리뷰받는 단계로 확장합니다. | 브랜치 이름, 커밋 메시지, PR 본문, 리뷰 반영 |
| Session 5 | 실수 복구와 작업 보관 | 협업 중 실수했을 때 작업을 되돌리거나 잠시 보관하는 기준을 익힙니다. | `restore`, `revert`, `reset`, `stash` |
| Session 6 | 협업 운영 규칙 정리 | 반복한 협업 흐름을 팀 브랜치 전략과 merge 방식으로 정리합니다. | GitHub Flow, merge 방식, tag, 체크리스트 |
| Session 7 | 기본기 보강 | PR 전 확인 습관을 `diff`, `log`, `.gitignore`로 구체화합니다. | `init`, `.gitignore`, `diff`, `log` |

## 📦 제출 규칙

| 세션 | 제출 파일 | 브랜치 | PR 제목 |
| --- | --- | --- | --- |
| Session 1 | `members/<본인GitHub아이디>/2026-04-24-git-session1.md` | `study/<아이디>-session1` | `docs: [git-session1] Git 기초와 첫 업로드` |
| Session 2 | `members/<본인GitHub아이디>/2026-04-26-git-session2.md` | `study/<아이디>-session2` | `docs: [git-session2] 브랜치와 PR 실습` |
| Session 3 | `members/<본인GitHub아이디>/YYYY-MM-DD-git-session3.md` | `study/<아이디>-session3` | `docs: [git-session3] 충돌과 merge 해결 실습` |
| Session 4 | `members/<본인GitHub아이디>/YYYY-MM-DD-git-session4.md` | `study/<아이디>-session4` | `docs: [git-session4] GitHub Flow와 PR 리뷰 워크플로우` |
| Session 5 | `members/<본인GitHub아이디>/YYYY-MM-DD-git-session5.md` | `study/<아이디>-session5` | `docs: [git-session5] 실수 복구와 stash 실습` |
| Session 6 | `members/<본인GitHub아이디>/YYYY-MM-DD-git-session6.md` | `study/<아이디>-session6` | `docs: [git-session6] 브랜치 전략과 협업 운영 정리` |
| Session 7 | `members/<본인GitHub아이디>/YYYY-MM-DD-git-session7.md` | `study/<아이디>-session7` | `docs: [git-session7] Git 기본기 보강 - init, ignore, diff, log` |

## 📚 세션 문서

- [Session 1](./session1.md): Git 설치 확인, 기본 명령어, 첫 업로드
- [Session 2](./session2.md): 브랜치, pull, PR 흐름 정리
- [Session 3](./session3.md): 롤링페이퍼 파일로 실제 충돌을 만들고 merge 해결 흐름 정리
- [Session 4](./session4.md): GitHub Flow, PR 작성, 리뷰 문화
- [Session 5](./session5.md): restore, revert, reset, stash 정리
- [Session 6](./session6.md): 브랜치 전략, merge 방식, 협업 체크리스트
- [Session 7](./session7.md): init, .gitignore, diff, log 기본기 보강

## 🔗 참고 문서

- 자세한 제출 절차는 [CONTRIBUTING.md](../CONTRIBUTING.md)를 참고하세요.
- 실제 리눅스 학습은 [week1/README.md](../week1/README.md)부터 시작합니다.

## 💡 초보자에게 중요한 점

- 완벽하게 이해하는 것보다 **직접 한 번 올려보는 경험**이 더 중요합니다.
- 중간에 막히면 혼자 오래 끌지 말고 질문하세요.
- `week0`는 Git 기초 준비 주차이고, 실제 리눅스 학습은 `week1`부터 시작합니다.
