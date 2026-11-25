# 05. 상황별 치트시트

명령어를 외우지 않아도 **하고 싶은 작업**을 기준으로 찾을 수 있도록 정리했습니다.

## 방금 수정한 파일을 커밋하고 싶을 때

```bash
git status
git add README.md
git commit -m "docs: update README"
```

## 내가 어느 브랜치에 있는지 모를 때

```bash
git branch --show-current
git status
```

## 새 기능을 별도 브랜치에서 만들고 싶을 때

```bash
git switch -c feature/new-page
```

## GitHub에 변경 사항을 올리고 싶을 때

```bash
git push -u origin feature/new-page
```

## 원격에 새로운 커밋이 있는지만 확인하고 싶을 때

```bash
git fetch origin
git log --oneline HEAD..origin/main
```

현재 브랜치가 `main`을 기반으로 작업하는 경우의 예시입니다. 원격 브랜치명은 실제 사용 환경에 맞추세요.

## 파일 수정 내용을 비교하고 싶을 때

```bash
git diff
git diff --staged
```

## 마지막 커밋들을 빠르게 보고 싶을 때

```bash
git log --oneline --graph --decorate -10
```

## 아직 커밋하지 않은 작업을 잠시 치워두고 싶을 때

```bash
git stash push -m "작업 임시 보관"
git stash list
git stash pop
```

기본 `stash`는 추적되지 않은 파일을 포함하지 않습니다. 필요하다면 `git stash push -u`를 검토하세요. `pop`에서 충돌이 나면 수동 해결이 필요할 수 있습니다.

## 방금 스테이징한 파일을 제외하고 싶을 때

```bash
git restore --staged README.md
```

스테이징만 취소하며 일반적으로 작업 디렉터리의 파일 수정 내용은 유지합니다.

## 충돌이 나서 병합을 중단하고 싶을 때

```bash
git status
git merge --abort
```

`merge`를 진행 중일 때 사용할 수 있습니다. `pull --rebase` 등 다른 작업 상황에서는 명령이 달라집니다.

## Git에 연결된 원격 주소가 궁금할 때

```bash
git remote -v
```

## 함께 보기

- [기본 명령어](./basics)
- [Branch & Merge](./branches)
- [원격 저장소](./remotes)
