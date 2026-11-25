# 01. 핵심 개념과 작업 흐름

## Git과 GitHub의 차이

- **Git**: 내 컴퓨터에서 프로젝트 변경 이력을 기록하고 비교하는 버전 관리 도구
- **GitHub**: 원격 Git 저장소를 호스팅하고 이슈, Pull Request 등을 통해 협업하는 플랫폼

Git은 GitHub 없이도 로컬에서 사용할 수 있습니다.

## 변경 사항이 거치는 세 영역

```text
Working Directory          Staging Area             Local Repository
  파일 편집       --add-->    커밋 후보       --commit-->   커밋 기록
       |                                                    |
       +--------------- git status -------------------------+
```

1. **Working Directory**: 현재 작업 중인 파일들
2. **Staging Area (Index)**: 다음 커밋에 포함하기로 선택한 변경 사항
3. **Local Repository**: `git commit`으로 기록된 변경 이력

원격 저장소(GitHub 등)는 별도이며 `git push`로 로컬 커밋을 보낼 수 있습니다.

## `add`와 `commit`을 구분하기

```bash
git add README.md
git commit -m "docs: README 설명 추가"
```

`add`는 파일을 곧바로 GitHub에 올리는 것이 아닙니다. 커밋 대상으로 **선택**하는 과정입니다. `commit`은 선택한 변경 내용을 **로컬 이력에 기록**합니다.

## 핵심 용어

| 용어 | 뜻 |
| --- | --- |
| Repository | Git이 버전 이력을 관리하는 저장소 |
| Commit | 특정 시점의 변경 내용과 메타데이터를 가리키는 기록 |
| Branch | 특정 커밋을 가리키는 이동 가능한 이름 |
| HEAD | 현재 체크아웃한 브랜치 또는 커밋을 가리키는 참조 |
| Remote | `origin` 같은 이름으로 등록한 원격 저장소 |
| Merge | 분리된 작업 이력을 합치는 작업 |

## 함께 보기

- [기본 명령어](./basics)
- [Branch & Merge](./branches)
