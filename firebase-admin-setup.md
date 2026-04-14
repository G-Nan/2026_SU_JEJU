# Firebase Admin Lock

현재 버전은 `admin.html`에 비밀번호 `0819`를 입력하면 관리자 화면이 열리는 구조입니다.

중요:
- 이 방식은 강한 보안이 아닙니다.
- 정적 사이트 + 비밀번호만으로는 Firebase Rules까지 안전하게 잠글 수 없습니다.
- 그래서 지금 rules는 전체 쓰기 허용 상태입니다.

현재 동작:
- `admin.html`에서 비밀번호 `0819` 입력 시 관리자 화면 열림
- 관리자 화면에서 회의일지/질문/답변 관리 가능
- 일반 사용자 화면에서는 수정 UI가 보이지 않음

정말 안전하게 잠그려면:
- Firebase Authentication 사용
- 관리자 계정 로그인
- Realtime Database Rules를 관리자 기준으로 제한
