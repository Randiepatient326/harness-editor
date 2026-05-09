# Harness Editor

> Claude Code의 `.claude/agents/*.md` 와 `.claude/skills/**/SKILL.md` 파일을
> 한 화면에서 시각적으로 보고 편집하는 단일 HTML 도구.

🌐 **바로 사용:** https://amazingsyp.github.io/harness-editor/harness-editor.html (Chrome / Edge 권장)

---

## 1분 안에 시작

1. 위 링크 클릭 (Chrome / Edge)
2. **📁 폴더 선택** → 프로젝트 루트(`.claude/` 폴더가 들어 있는 디렉토리) 선택
3. 좌측 트리에서 `.md` 파일 클릭 → 즉시 편집

데이터는 모두 **사용자 컴퓨터에만** 머무릅니다. 서버로 전송되지 않습니다 (브라우저 File System Access API 동작).

## 주요 기능

- 디렉토리 트리뷰 (에이전트·스킬·오케스트레이터 색상 구분, 변경/오류 마커)
- Frontmatter 폼 편집기 — `name` / `description` / `type` / `model` 필드별 입력
- Markdown 본문 에디터 + 분할 프리뷰 (좌·우 섹션 동기 스크롤)
- **직접 편집 모드 (WYSIWYG)** — 우측 프리뷰에서 표·헤딩·강조를 GUI로 편집
- 다중 파일 검색·일괄 치환 (정규식, 대상 필터)
- Description 적극성 점수·트리거 키워드 분석 (하네스 메타스킬 권장 패턴)
- 라운드트립 안전 직렬화 — `parse → 편집 → save` 시 의미 손실 0
- 다크/라이트 모드, 페이지 닫기 보호

## 지원 브라우저

| 브라우저 | 모드 |
|---------|------|
| Chrome / Edge / Brave / Opera | **디렉토리 모드** (권장) — 폴더 한 번 선택으로 다중 파일 직접 편집·저장 |
| Safari / Firefox | **단일 파일 모드** — 파일 업로드 → 편집 → 다운로드 |

## 단축키

| 키 | 동작 |
|----|------|
| `⌘S` | 현재 파일 저장 |
| `⌘⇧S` | 변경된 모든 파일 저장 |
| `⌘P` | 모든 파일 가로질러 검색 |
| `⌘⇧H` | 일괄 치환 |
| `⌘B` | 사이드바 토글 |
| `⌘\` | 프리뷰 토글 |
| `Esc` | 모달 닫기 |

## 로컬에서 직접 사용

레포 페이지에서 `harness-editor.html` 파일을 다운로드 후 더블클릭하면 됩니다. 외부 자원은 CDN뿐, 추가 설치 없음.

## 의존성 (모두 CDN)

- [marked.js](https://marked.js.org/) — Markdown 렌더링
- [js-yaml](https://github.com/nodeca/js-yaml) — Frontmatter YAML 파싱·직렬화
- [turndown](https://github.com/mixmark-io/turndown) + GFM 플러그인 — WYSIWYG의 HTML→Markdown 역변환

## 영감

이 도구는 [revfactory/harness](https://github.com/revfactory/harness) 메타스킬이 만들어내는 `.claude/agents/`·`.claude/skills/` 파일 형식에 친화적으로 설계됐습니다. 다만 **모든 Claude Code 표준 에이전트/스킬 `.md` 파일**에서 동작합니다.

## 라이선스

[Apache License 2.0](LICENSE) — 자유롭게 사용·수정·재배포 가능. 상세는 LICENSE 파일 참조.
