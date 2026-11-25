# 04. 원격 저장소

GitHub와 로컬 저장소 사이에서 커밋을 주고받는 명령어를 정리했습니다.

## 원격 저장소 복제: `git clone`

```bash
git clone https://github.com/OWNER/REPO.git
```

기존 원격 저장소를 로컬로 복제하고, 보통 `origin`이라는 이름으로 원격을 등록합니다. 비공개 저장소라면 접근 권한과 인증이 필요합니다.

## 원격 확인 및 연결: `git remote`

```bash
git remote -v
git remote add origin https://github.com/OWNER/REPO.git
```

이미 `origin`이 있으면 `add` 대신 URL 변경이 필요할 수 있습니다.

```bash
git remote set-url origin https://github.com/OWNER/NEW-REPO.git
```

## 원격으로 보내기: `git push`

```bash
git push -u origin main   # main의 업스트림 추적 설정하며 푸시
git push                  # 추적 설정된 브랜치를 기본 설정대로 푸시
```

`push`는 로컬에 존재하는 커밋을 원격 저장소에 반영합니다. 네트워크 접근 및 쓰기 권한이 필요합니다.

## 변경 사항 가져오기: `git fetch`

```bash
git fetch origin
```

원격 브랜치의 최신 이력을 가져오되, **현재 작업 중인 브랜치에 자동으로 병합하지 않습니다**.

## 가져와 통합하기: `git pull`

```bash
git pull origin main
```

대체로 `fetch` 후 현재 브랜치로 변경 사항을 통합하는 과정입니다. 병합 또는 리베이스 동작은 설정과 옵션에 따라 달라집니다. 로컬과 원격 이력이 분기된 경우 통합 방식을 명시해야 할 수 있습니다.

## `fetch` / `pull` / `push` 비교

| 명령어 | 데이터 이동 | 현재 브랜치에 반영 |
| --- | --- | --- |
| `git fetch` | 원격 → 로컬의 원격 추적 정보 | 자동으로 통합하지 않음 |
| `git pull` | 원격 → 로컬 | 가져온 뒤 통합 시도 |
| `git push` | 로컬 → 원격 | 원격 브랜치를 갱신 |

## 비공개 저장소 접근

비공개 GitHub 저장소를 다른 노트북에서 사용하려면 그 노트북에서도 GitHub 인증을 설정하고, `git clone` 또는 `git pull`을 사용하세요.

## 함께 보기

- [핵심 개념](./concepts)
- [상황별 치트시트](./cheatsheet)
