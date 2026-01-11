# Claude Code Workflow

<img width="1666" height="928" alt="image" src="https://github.com/user-attachments/assets/c9e17942-bc0a-4c5b-957b-d92c6799cce1" />

Claude Code의 핵심 사용 원칙과 생산성 높은 워크플로 구축 방법에 대한 연구 저장소입니다.

## 목차

- [시작하기](#시작하기)
- [핵심 원칙](#핵심-원칙)
- [워크플로 패턴](#워크플로-패턴)
- [예제](#예제)
- [기여하기](#기여하기)

## 시작하기

Claude Code를 효과적으로 사용하기 위한 기본 가이드는 [docs/getting-started.md](docs/getting-started.md)를 참조하세요.

## 핵심 원칙

Claude Code를 사용할 때 지켜야 할 핵심 원칙들입니다:

1. **명확한 컨텍스트 제공** - CLAUDE.md 파일로 프로젝트 컨텍스트를 제공
2. **점진적 작업** - 큰 작업을 작은 단위로 분할
3. **검증 주기** - 코드 변경 후 빌드/테스트 실행
4. **효과적인 프롬프트** - 구체적이고 명확한 지시

자세한 내용은 [docs/principles.md](docs/principles.md)를 참조하세요.

## 워크플로 패턴

| 워크플로 | 설명 | 문서 |
|----------|------|------|
| 코드 리뷰 | PR 리뷰 및 피드백 워크플로 | [workflows/code-review.md](workflows/code-review.md) |
| 디버깅 | 버그 분석 및 수정 워크플로 | [workflows/debugging.md](workflows/debugging.md) |
| 리팩토링 | 코드 개선 및 리팩토링 워크플로 | [workflows/refactoring.md](workflows/refactoring.md) |

## 예제

### Hooks
Claude Code 훅을 활용한 자동화 예제들입니다.
- [examples/hooks/](examples/hooks/)

### MCP 서버
MCP 서버 설정 및 활용 예제입니다.
- [examples/mcp/](examples/mcp/)

### 프롬프트
효과적인 프롬프트 작성 예제입니다.
- [examples/prompts/](examples/prompts/)

## 템플릿

프로젝트에서 바로 사용할 수 있는 템플릿들입니다.
- [templates/CLAUDE.md](templates/CLAUDE.md) - 프로젝트별 CLAUDE.md 템플릿

## 기여하기

이 저장소에 기여하고 싶으시다면:

1. 이 저장소를 Fork합니다
2. 기능 브랜치를 생성합니다 (`git checkout -b feature/amazing-feature`)
3. 변경사항을 커밋합니다 (`git commit -m 'feat: Add amazing feature'`)
4. 브랜치에 Push합니다 (`git push origin feature/amazing-feature`)
5. Pull Request를 생성합니다

## 라이선스

MIT License - 자유롭게 사용, 수정, 배포할 수 있습니다.

## 참고 자료

- [Claude Code 공식 문서](https://docs.anthropic.com/claude-code)
- [Anthropic 개발자 블로그](https://www.anthropic.com/engineering)
