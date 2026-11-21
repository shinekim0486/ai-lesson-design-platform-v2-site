# CHECKS — 테스트 체크리스트

검토 기준: Solar Work 기반 AI 개발 검토 표준지침 v1.0  
최종 검토일: 2026-11-21

## P00–P01 환경 준비

| 항목 | 결과 | 비고 |
|------|------|------|
| 프로젝트 폴더·실행 경로 확인 | PASS | 단일 HTML, 별도 서버 불필요 |
| 설치 환경 확인 | PASS | Flask 없음, 브라우저만으로 실행 |
| 기존 파일·환경설정 보존 | PASS | 전용 localStorage 키 사용 |

## W00–W02 요구사항·개발 계획

| 항목 | 결과 | 비고 |
|------|------|------|
| 사용 목적·대상 명확 | PASS | 교사/학생/관리자 역할 명확 |
| PRD.md 존재 | PASS | 2026-11-21 작성 완료 |
| PLAN.md 존재 | PASS | 2026-11-21 작성 완료 |
| 제외 범위 명시 | PASS | PRD.md 제외 범위 항목 작성 |

## W03-A 화면 구현

| 항목 | 결과 | 비고 |
|------|------|------|
| 입력·버튼·목록 표시 | PASS | 6개 탭 정상 구현 |
| 빈 목록 안내 | PASS | empty-state 클래스 처리 |
| 실제 화면 확인 | PASS | GitHub Pages 배포 완료 |

## W03-B 입력 검증·목록 추가

| 항목 | 결과 | 비고 |
|------|------|------|
| 필수 입력 검증 (제목, 목표) | PASS | trim() 후 빈값 거부 |
| 글자 수 제한 | PASS | maxlength 전 필드 설정 완료 |
| XSS 방어 | PASS | escapeHtml() 일관 적용 |
| 중복 저장 방지 | NOT_TESTED | 추후 확인 필요 |
| 서버 연결 실패 처리 | PASS | 목업 단계, API 미연동 |
| 사용자 입력 안전 출력 | PASS | escapeHtml() 적용 확인 |

## W03-C 저장 유지

| 항목 | 결과 | 비고 |
|------|------|------|
| 앱 전용 키 사용 | PASS | aiPlatformV4, aiPlatformUsers, aiPlatformSession |
| 새로고침 후 유지 | PASS | loadState()로 복원 |
| 서버 재실행 후 유지 | PASS | 서버 없는 구조 |
| 기존 데이터 보존 | PASS | try/catch로 파싱 오류 처리 |
| 저장 실패 사용자 알림 | PASS | 빨간 토스트 메시지 4초 표시 |

## W04 테스트

| 항목 | 결과 | 비고 |
|------|------|------|
| 정상 데이터 저장·확인 | PASS | 코드 흐름 확인 |
| 빈 값·공백 거부 | PASS | trim() 적용 |
| 경계값 테스트 (maxlength) | PASS | 각 필드 maxlength 설정 완료 |
| 오류 수정 후 재검증 | PASS | renderLesson 오류 수정 후 재확인 |
| CHECKS.md 기록 | PASS | 이 파일 |

## W05 사용성·마무리

| 항목 | 결과 | 비고 |
|------|------|------|
| 개선 후보 기록 | PASS | REVIEW.md 참조 |
| 최소 수정 원칙 준수 | PASS | 문제 부분만 수정 |
| README 작성 | PASS | 2026-11-21 작성 완료 |
| PRD/PLAN/CHECKS 갱신 | PASS | 2026-11-21 갱신 완료 |

## 미완료·예정 항목

| 항목 | 상태 | 계획 |
|------|------|------|
| Upstage Solar API 연동 | NOT_TESTED | Phase 5 예정 |
| AI 모둠 추천 로직 | NOT_TESTED | Phase 5 예정 |
| 중복 저장 방지 | NOT_TESTED | 추후 구현 |
| 모바일 반응형 전체 검증 | NOT_TESTED | 추후 확인 |
