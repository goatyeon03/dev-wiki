# Git & GitHub

Git은 **파일 변경 이력을 기록하고 관리하는 버전 관리 시스템**입니다. GitHub는 Git 저장소를 원격에서 보관하고 협업할 수 있게 하는 서비스입니다.

빠르게 명령어를 찾으려면 [상황별 치트시트](./cheatsheet)부터 보세요.

## 어디부터 볼까?

| 알고 싶은 것 | 문서 |
| --- | --- |
| Git은 파일 변경을 어떻게 추적할까? | [핵심 개념과 작업 흐름](./concepts) |
| 코드를 저장하고 커밋하려면? | [기본 명령어](./basics) |
| 여러 작업을 나눠 개발하려면? | [Branch & Merge](./branches) |
| GitHub에 올리거나 가져오려면? | [원격 저장소](./remotes) |
| 상황에 맞는 명령어만 찾고 싶다면? | [상황별 치트시트](./cheatsheet) |

## 가장 자주 쓰는 명령어 6개

```bash
git status                 # 현재 상태 확인
git add .                  # 현재 디렉터리 아래 변경 사항 스테이징
git commit -m "메시지"    # 로컬 변경 이력 저장
git switch -c feature     # 새 브랜치 생성 및 이동
git pull origin main      # 원격 main의 변경 사항 가져와 통합
git push origin main      # 로컬 main을 원격으로 전송
```

> [!TIP] 검색 팁
> 검색창에 `commit`, `충돌`, `clone`, `stash`처럼 명령어 또는 문제 상황을 그대로 입력해 보세요.

## 출처

- [공식 Git 문서](https://git-scm.com/docs)
- [Pro Git 도서 (공식 무료 문서)](https://git-scm.com/book/ko/v2)

> [!NOTE] 예시 문서
> 이 챕터는 실제 강의자료를 아직 반영하지 않은 **초기 예제 콘텐츠**입니다. 제공된 강의자료는 검토 후 적절한 문서에 통합하고 출처를 표시합니다.
