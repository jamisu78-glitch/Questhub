# QuestHub

## What This Is

QuestHub는 스팀(Steam) 인디/중소 게임 개발사와 검증된 마이크로 인플루언서(구독자 500~5,000명)를 안전하게 연결하는 B2B 게임 크리에이터 마케팅 SaaS 플랫폼이다. 게임 키 배포부터 미션 기반 캠페인 관리, 성과 측정까지 원스톱으로 제공하며, 사기 위험 제로를 핵심 차별점으로 내세운다.

## Core Value

크리에이터 신원이 100% 검증된 안전한 환경에서, 게임 키 배포→미션 진행→성과 확인의 전체 사이클이 단일 플랫폼에서 완결되어야 한다.

## Requirements

### Validated

(None yet — ship to validate)

### Active

**크리에이터 측:**
- [ ] 치지직/유튜브/트위치 OAuth 2.0 소셜 로그인 및 채널 소유권 자동 검증
- [ ] Steam Web API 연동으로 스팀 계정 실재성 및 게임 라이브러리 확인
- [ ] 스팀 비공개 프로필 감지 시 공개 전환 가이드 및 가입 차단
- [ ] 캠페인 목록 조회 (게임명, 장르, 미션 요약, 보상, 필터링)
- [ ] 캠페인 상세 확인 및 클릭 한 번 참여 신청
- [ ] 승인 시 게임 키 자동 발급 (1인 1키, 마스킹 처리)
- [ ] 방송 VOD URL/리뷰 URL 등록으로 미션 완료 제출
- [ ] 미션 승인 후 보상(포인트) 확인
- [ ] 공개 프로필 (채널 정보, 완료 캠페인 이력, 신뢰도 점수)

**개발사 측:**
- [ ] 이메일/비밀번호 회원가입 + Steamworks Publisher ID 연결
- [ ] 캠페인 생성 (게임 정보, 미션 요구사항, 보상 유형, 모집 인원, 기간)
- [ ] 스팀 게임 키 CSV/텍스트 대량 업로드 및 자동 분배
- [ ] 캠페인별 신청자 목록 확인 및 승인/거절 (개별+일괄)
- [ ] 성과 대시보드 (키 배포 현황, 미션 진행률, 콘텐츠 현황, 노출 성과 지표)
- [ ] 먹튀 방지 (미완료 자동 플래그, 키 폐기 명단 CSV 추출, 블랙리스트)
- [ ] 미션 QC (브론즈/실버: 개발사 수동 검수, 골드+: 자동 승인)

**시스템:**
- [ ] 자동 승인 티어제 (브론즈→실버→골드→플래티넘, 동시 퀘스트 제한)
- [ ] 알림 시스템 (in-app + 이메일)
- [ ] 스팀 리뷰 보상 금지 정책 시스템 적용 (키워드 자동 차단)
- [ ] 반려 가이드라인 및 크리에이터 보호 정책 (부당 반려 모니터링)
- [ ] 게임 키 암호화 저장 및 Rate Limiting

### Out of Scope

- Phase 2 비딩 마켓플레이스 — MVP에서 티어 데이터 축적 후 진행
- 실시간 채팅 — 높은 복잡도, 코어 가치 아님
- 모바일 앱 — 웹 퍼스트, 모바일은 후순위
- PG 연동/에스크로 — Phase 2 월 거래액 1천만원 초과 시 도입
- AI 자동 QC — 향후 확장 검토
- 역제안(크리에이터→개발사) — Phase 3
- 크리에이터 현금 보상/기프티콘 — 초기는 포인트 시스템만

## Context

**도메인:** B2B 게임 크리에이터 마케팅 (Steam 생태계 특화)

**타겟 사용자:**
- 개발사: 연 매출 $100K~$2M 스팀 인디/중소 게임 개발사, 마케팅 전담 0~1명
- 크리에이터: 치지직/유튜브 쇼츠/트위치 기반 게임 스트리머, 구독자 500~5,000명

**핵심 문제:**
- 개발사: 글로벌 UA 비용 급등($2~5/위시리스트), Key Reseller 피해, 운영 부담(수십 명 개별 관리)
- 크리에이터: 스폰서십 편중(10만+ 대형만), 신작 접근 기회 부족, 수익화 창구 부재

**규제 준수:**
- Valve Steamworks 가이드라인: 스팀 리뷰 보상 절대 금지
- FTC 가이드라인: 보상 조건 긍정적 리뷰 요구 및 인센티브 미공개 금지

**팀 경쟁 우위:**
- 'Tank Arena', 'Spectral Scream' 등 스팀 게임 직접 퍼블리싱 경험
- 도그푸딩 가능: 자체 IP로 첫 캠페인 검증
- VR 및 콘솔 게임 글로벌 런칭 경험

**초기 시장 진입:**
1. 1순위: 한국 스팀 인디 개발사 + 치지직/유튜브 쇼츠 스트리머
2. 2순위: 일본/동남아
3. 3순위: 북미/유럽 영어권 (Twitch 중심)

**KPI 목표:**
- 3개월: 크리에이터 100명, 활성 개발사 5곳, 미션 완료율 60%
- 6개월: 크리에이터 500명, 활성 개발사 30곳, 미션 완료율 75%

**보상 정책 (MVP):**
- 기본 보상: 게임 키 (개발사 제공, 0원)
- 추가 보상: QuestHub 포인트 (플랫폼 마케팅 예산 월 100만원 이내)
- 선택적: 개발사가 캠페인 생성 시 추가 보상 설정 가능

**비즈니스 모델:**
- Phase 1: 무료 + 성과 수수료 (미션 완료 건당)
- Phase 2: 프리미엄 슬롯 + 비딩 커미션 10~15%
- Phase 3: SaaS 구독 + 비딩 + 데이터 판매

## Constraints

- **Tech Stack**: Next.js (React) + TypeScript 프론트엔드, Node.js (NestJS) + TypeScript 백엔드, PostgreSQL + Redis — PRD에서 결정됨
- **Infra**: Vercel + Supabase (MVP 속도 우선, 서버리스)
- **Timeline**: 12주 로드맵 (W1~W12)
- **Team**: 기획/PM 1명, 백엔드 1명, 프론트엔드 1명, 디자인 0.5명(외주)
- **Budget**: 인건비 3,000~4,500만원, 외주 디자인 300~500만원, 인프라 월 30~50만원
- **OAuth**: 치지직/유튜브/트위치 개발자 앱 등록 아직 시작 전 — W1~W2에 선행 필요
- **Valve Compliance**: 스팀 리뷰 보상 절대 금지 — 시스템적으로 차단 필수
- **Design**: 와이어프레임/UI 키트 없음 — 스크래치부터 제작

## Key Decisions

| Decision | Rationale | Outcome |
|----------|-----------|---------|
| Vercel + Supabase 인프라 선택 | 12주 타임라인 + 3명 소규모 팀에서 서버리스 우선 | — Pending |
| Full MVP scope 구현 | PRD 4장 전체 기능 포함 (크리에이터+개발사+티어제+알림+먹튀방지) | — Pending |
| 초기 보상은 게임 키 + 포인트만 | 현금 보상은 Phase 2에서 비딩과 함께 도입 | — Pending |
| 치지직 + 유튜브 우선 | 한국 시장 1순위 타겟, 트위치는 후순위 | — Pending |
| NestJS 백엔드 | 프론트엔드와 언어 통일, 구조화된 모듈 시스템 | — Pending |

## Evolution

This document evolves at phase transitions and milestone boundaries.

**After each phase transition** (via `/gsd-transition`):
1. Requirements invalidated? → Move to Out of Scope with reason
2. Requirements validated? → Move to Validated with phase reference
3. New requirements emerged? → Add to Active
4. Decisions to log? → Add to Key Decisions
5. "What This Is" still accurate? → Update if drifted

**After each milestone** (via `/gsd-complete-milestone`):
1. Full review of all sections
2. Core Value check — still the right priority?
3. Audit Out of Scope — reasons still valid?
4. Update Context with current state

---
*Last updated: 2026-04-09 after initialization*
