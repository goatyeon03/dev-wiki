# Personal Dev Wiki (Git 챕터 시제품)

VitePress + Markdown 기반 읽기 전용 개인 개발 위키입니다.

## 요구사항

- Node.js 20 이상 (권장: Node.js 최신 LTS)
- npm

## 로컬 실행

```bash
npm install
npm run docs:dev
```

터미널에 출력되는 로컬 주소(일반적으로 `http://127.0.0.1:5173`)를 브라우저에서 열어보세요.

### 정적 사이트 빌드 테스트

```bash
npm run docs:build
npm run docs:preview
```

빌드 결과물은 `docs/.vitepress/dist/` 폴더에 생성됩니다.

## 내용 추가

- 새 개념: `docs/영역명/문서명.md` Markdown 파일 추가
- 목차: `docs/.vitepress/config.mts`의 `sidebar`, `nav` 수정
- 메인 카테고리: `docs/index.md`의 `features` 수정
- 강의자료 출처는 해당 문서 하단에 연결
- 예시 문서는 실제 강의자료 기반 정리가 아닌 초안임

## GitHub에 저장

이 저장소는 기존 개인 프로젝트와 분리된 비공개 저장소에 올리는 것을 권장합니다.

```bash
git init
git add .
git commit -m "docs: initialize personal dev wiki"
git branch -M main
git remote add origin https://github.com/goatyeon03/REPOSITORY-NAME.git
git push -u origin main
```

> `REPOSITORY-NAME`을 실제로 만든 **비공개 GitHub 저장소명**으로 교체하세요. 이 프로젝트 파일이 자동으로 GitHub에 업로드되지는 않습니다.

## 데이터 보존

문서 내용은 `docs/**/*.md` 파일로 보존됩니다. 변경 파일을 GitHub에 커밋/푸시하면 다른 노트북에서도 클론/풀로 동기화할 수 있습니다. 정적 페이지에는 메모나 체크박스를 저장하는 기능을 넣지 않았습니다.
