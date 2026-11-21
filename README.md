# AI 수업설계 지원 플랫폼 v4

## 프로젝트 개요
직업계고 교사를 위한 AI 활용 수업설계 지원 웹 플랫폼입니다.  
티처스 캔버스(역공학 모델) 기반 9개 항목으로 수업을 한 화면에 기획합니다.

## 사용 대상
- 직업계고 교사 (수업설계, 성찰 일지, 소시오그램)
- 학생 (AI 튜터 대화, 설문, 대시보드)
- 관리자 (학생 관리, 공지 등록)

## 주요 기능
| 탭 | 기능 |
|----|------|
| 수업 아이디어 | 아이디어 등록 및 목록 관리 |
| 수업설계 | 티처스 캔버스 9항목 기획, 활동 유형별 자동 입력 |
| AI 튜터 | 소크라테스식 AI 대화 (목업) |
| 연구 로그 | 수업 성찰 일지 작성 |
| 대시보드 | XP·레벨·뱃지·활동 통계, PDF 인쇄 |
| 소시오그램 | 학생 관계 시각화, AI 모둠 추천 (목업) |

## 실행 방법
별도 서버 없이 브라우저에서 바로 실행 가능합니다.

**로컬 실행:**
```
index.html 파일을 브라우저로 열기
```

**배포 주소:**
```
https://shinekim0486.github.io/ai-lesson-design-platform-v2-site
```

## 기술 스택
- 순수 HTML + CSS + JavaScript (단일 파일)
- localStorage 기반 데이터 저장 (서버·DB 없음)
- GitHub Pages 배포

## 데이터 저장
- 모든 데이터는 브라우저 localStorage에 저장됩니다
- 같은 기기·같은 브라우저에서만 데이터가 유지됩니다
- localStorage 키: `aiPlatformV4`, `aiPlatformUsers`, `aiPlatformSession`

## 재시작 방법
1. 브라우저에서 배포 주소 접속
2. 로그인 후 이전 데이터 자동 복원
3. 데이터가 사라진 경우: 같은 브라우저인지 확인

## 폴더 구조
```
ai-lesson-design-platform-v2-site/
├── index.html          ← 메인 플랫폼 (전체 기능 포함)
├── flowchart_platform.html  ← 플랫폼 구조 흐름도
├── teacher-guide.html  ← 선생님 가이드 페이지
├── PRD.md              ← 요구사항 정의서
├── PLAN.md             ← 개발 계획
├── CHECKS.md           ← 테스트 체크리스트
├── REVIEW.md           ← AI 개발 검토 결과
└── README.md           ← 이 파일
```
