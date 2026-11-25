# 03. Branch & Merge

브랜치는 하나의 작업 이력에서 새로운 작업 흐름을 나누기 위해 사용하는 포인터입니다.

## 브랜치 목록: `git branch`

```bash
git branch       # 로컬 브랜치 목록
git branch -a    # 원격 추적 브랜치 포함
git branch -vv   # 추적 관계 및 마지막 커밋
```

현재 브랜치에는 `*` 표시가 붙습니다.

## 생성 및 이동: `git switch`

```bash
git switch -c feature/login   # 새 브랜치 생성 후 이동
git switch main               # main으로 이동
```

`git branch feature/login`은 브랜치만 생성합니다. 브랜치 전환에는 `git switch`를 사용합니다.

## 병합: `git merge`

`feature/login`의 작업을 `main`에 합치려면:

```bash
git switch main
git merge feature/login
```

병합 시점과 이력에 따라 **fast-forward** 또는 **merge commit** 형태로 진행됩니다.

## 충돌(conflict)이 발생하면?

같은 부분을 양쪽에서 다르게 수정했을 때 충돌이 발생할 수 있습니다.

```text
<<<<<<< HEAD
main 브랜치의 내용
=======
feature 브랜치의 내용
>>>>>>> feature/login
```

충돌 마커를 제거하고 원하는 최종 내용을 작성한 뒤:

```bash
git status
git add 충돌난파일.md
git commit                   # 일반 병합 충돌을 수동 해결한 경우
```

> [!TIP]
> 병합을 중단하고 이전 상태로 돌아가려면 `git merge --abort`를 사용할 수 있습니다. 단, 병합 전에 미커밋 변경 사항이 있었다면 복구가 복잡할 수 있어 먼저 작업 상태를 확인하세요.

## 브랜치 삭제

```bash
git branch -d feature/login  # 이미 병합된 브랜치를 안전하게 삭제
git branch -D feature/login  # 병합 여부와 무관하게 강제 삭제 (주의)
```

## 함께 보기

- [원격 저장소](./remotes)
- [상황별 치트시트](./cheatsheet)
