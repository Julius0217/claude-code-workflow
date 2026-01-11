# 버그 수정 프롬프트

## 에러 분석

### 런타임 에러
```
다음 에러가 발생해:

TypeError: Cannot read property 'map' of undefined
    at UserList (src/components/UserList.tsx:15:23)
    at renderWithHooks (node_modules/react-dom/...)

이 에러의 원인을 분석하고 수정해줘.
```

### 빌드 에러
```
npm run build 실행 시 다음 에러가 발생해:

TS2345: Argument of type 'string | undefined' is not assignable
to parameter of type 'string'.

src/utils/api.ts:42:15 - error TS2345

원인을 분석하고 타입 안전하게 수정해줘.
```

### 테스트 실패
```
npm test 실행 시 다음 테스트가 실패해:

FAIL src/services/auth.test.ts
  ● AuthService › login › should return user on valid credentials

    expect(received).toEqual(expected)
    Expected: {"id": 1, "email": "test@test.com"}
    Received: undefined

테스트 코드와 실제 구현을 분석해서 문제를 수정해줘.
```

## 동작 버그

### 예상과 다른 동작
```
문제:
- 기대 동작: 로그인 후 대시보드로 리다이렉트
- 실제 동작: 로그인은 성공하지만 현재 페이지에 머무름

관련 파일:
- src/pages/Login.tsx
- src/hooks/useAuth.ts
- src/contexts/AuthContext.tsx

원인을 찾아서 수정해줘.
```

### 간헐적 버그
```
문제: 가끔 API 호출이 두 번 발생함
조건: React Strict Mode에서만 발생하는 것 같음
증상: 네트워크 탭에서 같은 요청이 두 번 보임

src/hooks/useFetch.ts를 분석해서 원인을 찾고 수정해줘.
```

## 성능 버그

### 느린 렌더링
```
Dashboard 페이지가 데이터 로딩 후 렌더링이 느려.
React DevTools Profiler에서 불필요한 리렌더링이 보임.

src/pages/Dashboard.tsx를 분석하고 최적화해줘.
memo, useMemo, useCallback 적용이 필요한 부분을 찾아줘.
```

### 메모리 누수
```
SPA에서 페이지 이동 시 메모리가 계속 증가해.
Chrome DevTools 메모리 탭에서 detached DOM nodes가 증가함.

컴포넌트의 cleanup 로직을 검토하고 메모리 누수를 수정해줘.
```

## 호환성 버그

### 브라우저 호환성
```
Safari에서 날짜 파싱이 안 돼:
new Date('2024-01-15') → Invalid Date

Safari 호환되도록 수정해줘.
```

### 모바일 이슈
```
모바일에서 드롭다운 메뉴가 화면 밖으로 나가.
viewport를 고려해서 메뉴 위치를 조정하는 로직을 추가해줘.
```
