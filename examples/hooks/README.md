# Claude Code Hooks 예제

Claude Code 훅을 활용한 자동화 예제입니다.

## 훅 개요

Claude Code는 다양한 이벤트에 반응하는 훅을 지원합니다:

- `PreToolUse` - 도구 실행 전
- `PostToolUse` - 도구 실행 후
- `Notification` - 알림 발생 시
- `Stop` - 작업 완료 시

## 설정 위치

```
~/.claude/settings.json
```

## 예제 목록

1. [auto-lint.json](auto-lint.json) - 파일 수정 후 자동 린트
2. [commit-guard.json](commit-guard.json) - 커밋 전 검증
3. [notification-slack.json](notification-slack.json) - Slack 알림 연동
4. [test-runner.json](test-runner.json) - 테스트 자동 실행
