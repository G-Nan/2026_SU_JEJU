# 2026 SU JEJU

정적 페이지 + Firebase Realtime Database로 운영하는 캠프 사이트입니다.

## 운영 방식

- 공개 페이지: `index.html`, `log.html`, `opinions.html`
- 관리자 페이지: `admin.html`
- 초기 데이터 입력과 이후 수정은 모두 `admin.html`에서 진행
- `firebase-seed.json`은 참고용 로컬 데이터 파일로만 보관

## 관리자 페이지

- 파일: `admin.html`
- 현재 비밀번호: `0819`
- 관리 가능 항목:
  - 회의일지
  - 질문
  - 답변

## Firebase 관련

- 현재 공개 페이지와 관리자 페이지는 Firebase Realtime Database를 직접 읽고 씁니다.
- 별도 자동 업로드 스크립트는 사용하지 않습니다.
- 운영 데이터의 기준은 Firebase입니다.

## 주의

- 현재 관리자 보호는 강한 보안이 아닙니다.
- 프론트엔드 비밀번호 방식이라 실제 접근 제어가 아니라 화면 잠금에 가깝습니다.
- 실제 운영 보안이 필요하면 Firebase Authentication + Rules 제한으로 바꿔야 합니다.
