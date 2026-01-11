# 코드 작성 프롬프트

## 새 기능 구현

### API 엔드포인트
```
다음 요구사항에 맞는 REST API 엔드포인트를 구현해줘:
- 경로: POST /api/users/register
- 입력: { email, password, name }
- 검증: 이메일 형식, 비밀번호 8자 이상
- 응답: 생성된 사용자 정보 (비밀번호 제외)
- 에러: 중복 이메일 시 409 반환

기존 프로젝트의 코딩 스타일과 에러 처리 패턴을 따라줘.
```

### React 컴포넌트
```
다음 요구사항의 React 컴포넌트를 구현해줘:
- 컴포넌트명: UserProfileCard
- Props: user (id, name, email, avatar)
- 기능: 프로필 이미지, 이름, 이메일 표시
- 스타일: 기존 프로젝트의 Tailwind 클래스 사용
- 접근성: 적절한 aria 속성 포함
```

### 유틸리티 함수
```
다음 유틸리티 함수를 구현해줘:
- 함수명: debounce
- 파라미터: func (함수), wait (밀리초)
- 반환: 디바운스된 함수
- 타입: 제네릭으로 원본 함수 타입 유지
- 추가: cancel 메서드 포함
```

## 기존 기능 확장

### 기능 추가
```
src/services/email.ts의 sendEmail 함수에 다음 기능을 추가해줘:
- 첨부파일 지원 (최대 5개, 각 10MB 이하)
- 재시도 로직 (최대 3회, 지수 백오프)
- 전송 결과 로깅

기존 인터페이스와 호환성을 유지해줘.
```

### 옵션 추가
```
formatDate 함수에 다음 옵션을 추가해줘:
- locale: 'ko-KR' | 'en-US' (기본값: 'ko-KR')
- includeTime: boolean (기본값: false)
- relative: boolean (기본값: false) - "3일 전" 형식

기존 호출부는 수정 없이 동작해야 해.
```

## 통합 작업

### 외부 API 연동
```
Stripe 결제 API를 연동하는 서비스를 구현해줘:
- 파일: src/services/payment.ts
- 기능: 결제 생성, 취소, 환불
- 환경변수: STRIPE_SECRET_KEY 사용
- 에러 처리: Stripe 에러를 커스텀 에러로 변환
- 테스트: 모킹 가능한 구조로 설계
```

### 데이터베이스 마이그레이션
```
users 테이블에 다음 컬럼을 추가하는 마이그레이션을 작성해줘:
- phone_number: varchar(20), nullable
- verified_at: timestamp, nullable
- preferences: jsonb, default {}

Prisma 마이그레이션 파일 형식으로 작성해줘.
```
