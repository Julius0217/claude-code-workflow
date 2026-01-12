# Claude Code Workflow

> Claude Code 사용 원칙과 워크플로우 연구 저장소 (문서 프로젝트)

## 프로젝트 특성

| 항목 | 값 |
|------|------|
| 유형 | 마크다운 문서 프로젝트 (코드 없음) |
| 언어 | 한국어 (기술용어 영어 병기) |
| 대상 | Claude Code 사용자/개발자 |

## 구조

```text
docs/           # 핵심 교육 문서
├── getting-started.md   # 입문 가이드
├── principles.md        # 7가지 핵심 원칙
└── best-practices.md    # 고급 활용법 (MCP, 훅, 팀 협업)

workflows/      # 실무 워크플로우 패턴 (4-5단계 프로세스)
├── code-review.md       # PR 리뷰
├── debugging.md         # 버그 분석
└── refactoring.md       # 코드 개선

examples/       # 실제 활용 예제
├── prompts/    # 5가지 프롬프트 카테고리
├── hooks/      # 자동화 훅 설정 (JSON)
└── mcp/        # MCP 서버 설정 (JSON)

templates/      # 복사용 템플릿 (다른 프로젝트용)
```

## 핵심 개념

| 개념 | 설명 | 참고 |
|------|------|------|
| 4대 원칙 | 컨텍스트, 점진적 작업, 검증, 프롬프트 | docs/principles.md |
| CLAUDE.md | 프로젝트 컨텍스트 파일 (전역→프로젝트→디렉토리) | templates/CLAUDE.md |
| MCP | 외부 시스템 연동 프로토콜 | examples/mcp/ |
| Hooks | 자동화 트리거 (PreToolUse, PostToolUse 등) | examples/hooks/ |

## 문서 컨벤션

- **구조**: 제목 → 개요 → 예제 → 체크리스트
- **예제 표기**: 나쁜 예 → 좋은 예 순서
- **코드 블록**: 언어 태그 필수 (`bash`, `json`, `typescript` 등)
- **비교**: 복잡한 비교는 마크다운 테이블 사용

## 품질 검증

```bash
# 마크다운 린트 (로컬)
npx markdownlint-cli "**/*.md"
```

GitHub Actions 자동 실행:

- `markdown-lint.yml` - 푸시/PR 시 스타일 검사
- `link-check.yml` - 깨진 링크 감지

## 작업 규칙

### 새 문서 추가 시

1. 기존 문서 스타일 참고 (헤더 구조, 표 형식)
2. 관련 문서에 링크 추가 (README.md 목차 등)
3. 마크다운 린트 통과 확인

### 예제 추가 시

1. 실제 동작 검증 후 추가
2. 민감 정보는 플레이스홀더 사용 (`your-api-key`, `<TOKEN>`)
3. 위험한 명령어에 경고 문구 추가

## 자주 요청되는 작업

| 요청 | 참고 파일 | 형식 |
|------|----------|------|
| 새 워크플로우 | workflows/*.md | 4-5단계 프로세스 + 체크리스트 |
| 프롬프트 예제 | examples/prompts/*.md | 카테고리별 분류, 구체적 예시 |
| hooks 예제 | examples/hooks/*.json | JSON, 실제 동작 가능해야 함 |
| MCP 설정 | examples/mcp/*.json | JSON, 설명 주석 포함 |

## 변경 시 연쇄 확인

| 변경 대상 | 확인 필요 |
|----------|----------|
| docs/ 구조 | README.md 목차, 내부 링크 |
| 새 카테고리 | .github/labeler.yml, 이슈 템플릿 |
| 워크플로우 추가 | README.md 워크플로 테이블 |

## 문서 학습 경로

```text
README.md (진입점)
    ↓
docs/getting-started.md (기본)
    ↓
docs/principles.md (심화)
    ↓
docs/best-practices.md (고급)
    ↓
workflows/ + examples/ (실무 적용)
```

## 주의사항

- API 키, 비밀번호 하드코딩 금지
- 실제 개인정보 포함 금지
- 보안 취약 예제 금지 (SQL 인젝션, `eval` 등)
- 기존 문서 스타일과 다른 형식 사용 금지
- 영어 전용 문서 금지 (한국어 필수)
