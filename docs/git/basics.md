# 02. 기본 명령어

Git 프로젝트를 시작하고 파일 변경을 기록할 때 가장 먼저 사용하는 명령어입니다.

## 저장소 만들기: `git init`

```bash
mkdir my-project
cd my-project
git init
```

현재 폴더에 `.git` 디렉터리가 생성되고 Git 이력 관리가 시작됩니다. 기존 원격 저장소를 내려받는 작업은 [`git clone`](./remotes#원격-저장소-복제-git-clone)을 사용합니다.

## 현재 상태 확인: `git status`

```bash
git status
```

변경된 파일, 스테이징된 파일, 아직 추적되지 않는 파일 등을 보여줍니다. 실습 중 예상과 다른 결과가 나오면 가장 먼저 확인하세요.

## 스테이징: `git add`

```bash
git add README.md       # 특정 파일
git add .               # 현재 디렉터리 이하의 변경 사항
git add -A              # 저장소 전체의 추가·수정·삭제 반영
```

> [!WARNING] 주의
> `git add .`는 상황에 따라 비밀키나 큰 파일까지 포함할 수 있습니다. `git status`로 확인하고, `.env` 등 민감한 파일은 `.gitignore`로 제외하세요. 이미 추적 중인 파일은 `.gitignore`만 추가해도 추적이 중단되지 않습니다.

## 커밋: `git commit`

```bash
git commit -m "docs: Git 기본 명령어 추가"
```

커밋은 로컬 저장소의 이력을 기록합니다. GitHub에 반영하려면 [`git push`](./remotes#원격으로-보내기-git-push)가 필요합니다.

## 이력 확인: `git log`

```bash
git log --oneline --graph --decorate -10
```

가장 최근 10개 커밋을 한 줄씩 트리 형태로 보여줍니다.

## 변경 내용 비교: `git diff`

```bash
git diff                  # 아직 스테이징하지 않은 변경
git diff --staged         # 다음 커밋에 포함할 변경
```

## 파일 무시: `.gitignore`

프로젝트 최상위 `.gitignore` 예시:

```gitignore
.env
.venv/
__pycache__/
node_modules/
.DS_Store
```

환경설정 비밀값이나 생성 파일을 불필요하게 커밋하지 않도록 지정합니다. 이미 커밋한 비밀값은 별도의 제거 및 키 교체 조치가 필요합니다.

## 실습 흐름

```bash
git init
git status
git add README.md
git diff --staged
git commit -m "docs: first commit"
git log --oneline
```

## 함께 보기

- [핵심 개념](./concepts)
- [원격 저장소](./remotes)
