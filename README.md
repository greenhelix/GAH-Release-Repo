# GAH Release Repo

Google Auth Helper 설치 파일 배포 전용 저장소.

[![Version Linux](https://img.shields.io/badge/Linux-v1.2.13-blue)](linux/version.json)
[![Version Windows](https://img.shields.io/badge/Windows-v0.1.2-blue)](windows/version.json)
[![Version macOS](https://img.shields.io/badge/macOS-v1.0.23-blue)](macos/version.json)

---

## 저장소 구성

```
linux/
  gah-linux-amd64.deb     ← 최초 설치용 (항상 최신)
  gah-linux-x64.tar.gz    ← 자동 업데이트용 (항상 최신)
  version.json            ← 앱 내 자동 업데이트 메타데이터
  INSTALL.md              ← 설치 가이드

windows/
  gah-windows-x64.zip     ← 설치 패키지
  version.json

macos/
  gah-macos.tar.gz        ← 앱 번들
  version.json
```

---

## 설치 방법

**Linux (Ubuntu)**
```bash
sudo dpkg -i gah-linux-amd64.deb
```
→ 자세한 내용: `linux/INSTALL.md`

**Windows**
- `gah-windows-x64.zip` 압축 해제 후 `gah.exe` 실행

**macOS**
- `gah-macos.tar.gz` 압축 해제 후 `gah.app` 실행

**업데이트**
앱 실행 시 자동으로 신버전 감지 → 패키지 다운로드 후 재시작

---

## 현재 버전

| 플랫폼 | 버전 | 날짜 |
|--------|------|------|
| Linux | **v1.2.13** | 2026-07-22 |
| Windows | v0.1.2 | 2026-04-28 |
| macOS | v1.0.23 | 2026-05-04 |

---

## 버전 이력

### v1.x

| 버전 | 날짜 | 플랫폼 | 주요 변경 |
|------|------|--------|-----------|
| **v1.2.13** | 2026-07-22 | Linux | Jira 제거 + ATS 연결 진단(ufw·IP·헬스체크) + 테스트 등록 Tool 버전 필드 |
| **v1.2.11** | 2026-07-14 | Linux | ATS Webhook 히스토리 영속화 + 라이브 트래킹 (30초 폴링, RUNNING 배너) |
| **v1.2.10** | 2026-07-14 | Linux | ATS Webhook: FieldNameNotFound 수정 + ATS 상세 API로 실제 count 조회 |
| **v1.2.9** | 2026-07-14 | Linux | ATS Webhook: Hook 수신 후 ATS API 직접 조회로 전환 (빈 body 문제 해결) |
| **v1.2.8** | 2026-07-13 | Linux | F-013 ATS Webhook 수신 내장 (포트 8765) → Lark Base 자동 업로드, 히스토리 UI |
| **v1.2.7** | 2026-07-06 | Linux | FW 리포트 DB 조회 이중화, All Pass Upload 제거, 카드 메시지 Schema 2.0, app_secret 갱신 |
| **v1.2.6** | 2026-07-01 | Linux | 카드 메시지 schema 1.0 전환 (전송 오류 수정) + 에러 SelectableText |
| **v1.2.5** | 2026-07-01 | Linux | Bot 카드 메시지 schema 2.0 적용 (markdown 렌더링 정상화) |
| **v1.2.4** | 2026-07-01 | Linux | Bot 카드 메시지 (FW 진행 현황 + 결과 요약), 결과 메뉴 정리, DB 탭 제거 |
| **v1.2.3** | 2026-07-01 | Linux | Lark Base 숫자 필드 파싱 수정 (진행률/shard 정상 반영) |
| **v1.2.2** | 2026-06-30 | Linux | FW 통합 리포트 Lark Base 연동 (진행률 조회 + 프로그레스바 HTML 이메일), 테스트 등록 Base 업로드, 설정 정리 |
| **v1.2.1** | 2026-06-30 | Linux | 테스트 등록 UI 개선 (17개 항목 + 커스텀 추가), Jira 시작알림 제거, Base 테이블 필드명 정리 |
| **v1.2.0** | 2026-06-30 | Linux | 공유 메뉴 5탭 재편 (테스트 등록/DB/Lark/이메일/설정), Lark Bot 메신저 상태 공유, Redmine 완전 제거 |
| **v1.1.0** | 2026-06-18 | Linux | XTS 테스트 시간 정량화 (정밀 타이밍 파서/DB 마이그레이션), 실시간 shard 로그 표시, -m 모듈 정보, 리소스 최적화/dead code 정리 |
| **v1.0.61** | 2026-06-17 | Linux | 성능 분석 대시보드 (시간 트렌드/선형회귀/Shard 비교/병목 분석), ETA 개선, 실시간 현황 강화, retry 추적 |
| **v1.0.60** | 2026-06-17 | Linux | 실시간 현황 UI 개선 (레이아웃·타이머·상태바 제거), 터미널 Ctrl+Shift+줌 |
| **v1.0.59** | 2026-06-17 | Linux | PASS RATE / MODULE 바 indeterminate 애니메이션 제거 |
| **v1.0.58** | 2026-06-17 | Linux | retry 경과시간 고정, GTS 마지막 모듈 완료 감지, ETA 과대추정 수정 |
| **v1.0.57** | 2026-06-17 | Linux | retry ETA 정확도 개선: 전체 세션 합산 → 실제 실행 모듈 기반 동적 추정 |
| **v1.0.56** | 2026-06-17 | Linux | 대시보드 UI 개선: PASS RATE 4색 세그먼트 바, Shard 수영레인 그라데이션 카드, 레이스 커브 전체 타임라인 |
| **v1.0.55** | 2026-06-16 | Linux | 터미널 스크롤 수정, 대시보드 그래프 DB 기반 동작, retry 세션 실측 ETA |
| **v1.0.54** | 2026-06-15 | Linux | 대시보드 LIVE/기록 탭 분리, 레이스 커브·Shard 수영레인, DB 기반 ETA, auto_upload DB 단계 제거 |
| **v1.0.53** | 2026-06-15 | Linux | 실시간 현황 pass/fail 파싱 개선 (GTS/CTS 로그 포맷 기반) |
| **v1.0.52** | 2026-06-15 | Linux | Feishu Base 필드명 정리 + 오류 메시지 선택 가능 |
| **v1.0.51** | 2026-06-15 | Linux | Tool Version 페이지 개선 |
| **v1.0.50** | 2026-06-15 | Linux | 단색모드 마우스 스크롤 수정 + Tailscale 경고 배너 |
| **v1.0.49** | 2026-06-15 | Linux | Feishu Base 자동 업로드 + tmux 마우스 토글 + 실시간 현황 탭 |
| **v1.0.48** | 2026-06-11 | Linux | Jira 메뉴 비활성화 + Lark Base 테스트 데이터 자동 기록 |
| **v1.0.47** | 2026-06-09 | Linux | Wiki 문서 제목 {Suite}-{빌드버전}-{폴더명} 형식으로 변경 |
| **v1.0.46** | 2026-06-09 | Linux | Lark Drive → Wiki Space 전환 (결과 문서 Wiki 노드 생성) |
| **v1.0.45** | 2026-06-08 | Linux | Lark 결과 문서 실패 판정 수정 + 폴더 선택 UI |
| **v1.0.44** | 2026-06-08 | Linux | 결과 문서 생성 단계별 진행 상태 표시 |
| **v1.0.43** | 2026-06-08 | Linux | Lark 결과 문서 실패 목록 파싱 개선 |
| **v1.0.42** | 2026-06-08 | Linux | Lark 업로드/문서 생성 버그 수정 |
| **v1.0.41** | 2026-06-08 | Linux | Lark Drive 업로드 + 결과 문서 생성 기능 추가 |
| **v1.0.40** | 2026-06-06 | Linux | YTS DB 관리 목록 미리보기 제거 |
| **v1.0.39** | 2026-06-04 | Linux | Tools 메뉴 개편 + YTS 명령어 생성 기능 추가 |
| **v1.0.38** | 2026-05-26 | Linux | Supabase → 로컬 PostgreSQL(PostgREST) 이전 |
| **v1.0.37** | 2026-05-15 | Linux | 터미널 뷰 가독성 개선 (폰트 크기↑, 패딩, 커서 스타일) |
| **v1.0.36** | 2026-05-14 | Linux | 대시보드 실시간 트래킹 (tmux capture-pane) + 물결 Pass Rate UI |
| **v1.0.35** | 2026-05-14 | Linux | l i 상태바 ANSI 파싱 수정 + tmux 마우스 설정 안내 다이얼로그 |
| **v1.0.34** | 2026-05-13 | Linux | 스크롤 수정 + PTY 중복 연결 방지 + 로그파서 FAILED 감지 + 직접실행 레이아웃 |
| **v1.0.33** | 2026-05-13 | Linux | 터미널 세션 race condition 수정 + 색상 토글 + UI 2행 개편 + 하단 상태바 |
| **v1.0.32** | 2026-05-13 | Linux | 로그 분석 탭 추가 — 터미널/로그 분석 듀얼 탭, 드래그 복사 지원 |
| **v1.0.31** | 2026-05-13 | Linux | tmux 세션 자동 정리 + 로그 화면 개선 (wrap 토글, 색상 분리) |
| **v1.0.30** | 2026-05-11 | Linux | F-011 Jira 업로드 UI 멈춤 수정 — SAX 파서 + Isolate 파싱 + 모듈 진행률 표시 |
| **v1.0.28** | 2026-05-07 | Linux | F-011 테스트 결과 필드(customfield_10159) 업로드 연결 — 진행률 editmeta 방식 수정 / 커스텀 필드 업데이트 분리 |
| **v1.0.27** | 2026-05-07 | Linux | F-011 세션 선택 버그 수정 / 업로드 폼 2-column 박스 UI 재설계 |
| **v1.0.26** | 2026-05-07 | Linux | F-011 진행률 반내림 수정 / CTS-on-GSI 자동 감지 / FW 다이얼로그 / 미리보기 스크롤 |
| **v1.0.25** | 2026-05-06 | Linux | F-011 팝업 세션 선택 / XML 전체 파싱 / Jira ADF+커스텀필드 |
| **v1.0.24** | 2026-05-05 | Linux | F-011 결과 업로드 탭 UX 개선 |
| **v1.0.23** | 2026-05-04 | macOS | macOS 배포 지원 추가 — 네이티브 앱 / 자동 업데이트 / ADB Controller / GitHub Actions |
| **v1.0.22** | 2026-05-01 | 전체 | 해결방안 UI 개선 — 텍스트 선택 / 자동 새로고침 / F-012 feature 정비 |
| **v1.0.21** | 2026-04-28 | 전체 | Jira 업무생성 개선 (TestType/FW 버전 패널/인증 유형 자동 선택) / Windows 자동 업데이트 지원 |
| **v1.0.20** | 2026-04-26 | 전체 | Jira 결과 공유 개선 — ADF 3섹션 구조 / 진행률 드롭다운 / TestType 레이블 |
| **v1.0.18** | 2026-04-23 | Linux | ADB Controller — 파일 탐색기 탭 추가 (탐색/Pull/삭제) |
| **v1.0.17** | 2026-04-23 | Linux | ADB Controller — adb 경로 탐색 수정 |
| **v1.0.16** | 2026-04-23 | Linux | ADB Controller — PATH 해결 버그 수정 + 디버깅 로그 강화 |
| **v1.0.15** | 2026-04-22 | Linux | ADB Controller — Key Events 접기/펼치기 + 숫자패드 추가 |
| **v1.0.14** | 2026-04-22 | Linux | ADB Controller 탭 추가 — 디바이스 선택 / scrcpy / Key Events / Quick Commands / File Push |
| **v1.0.3** | 2026-04-16 | 전체 | F-010 해결방안 트리뷰 재설계 — Suite/Module/TestCase 3단계 탐색 |
| **v1.0.2** | 2026-04-15 | 전체 | Jira F-010 수정 — FW 에픽 매칭 / ADF expand / Confluence 링크 |
| v1.0.1 | 2026-04-14 | 전체 | Jira 결과 공유 기능 추가 — FW 에픽 자동 검색 + ADF 결과 테이블 |
| **v1.0.0** | 2026-04-13 | 전체 | 공식 릴리즈 — XTS 툴 버전 현황 탭 / FW 리포트 Waiver 처리 |

### v0.x

| 버전 | 날짜 | 플랫폼 | 주요 변경 |
|------|------|--------|-----------|
| v0.9.9 | 2026-04-11 | 전체 | 이메일 진행바 모듈기반 수정 / 잠금화면 개선 / Dashboard 수정 |
| v0.9.8 | 2026-04-11 | 전체 | FW 리포트 인증 유형 선택 / 테스트 기간 표시 |
| v0.9.4 | 2026-04-10 | 전체 | F-006 FW 버전별 통합 인증 리포트 이메일 공유 기능 추가 |
| **v0.8.7** | 2026-04-09 | 전체 | F-003 Select Device / retry 방식 개선 / F-006 이메일 Incomplete Modules 수정 |
| **v0.8.0** | 2026-04-07 | 전체 | F-003 retry 폴백 수정 / Quick cmd 버튼 / F-011 Jira 업무생성 |
| v0.7.6 | 2026-04-06 | 전체 | 이메일 최근 수신자 저장 / Python bridge→Dart mailer 교체 |
| v0.7.3 | 2026-04-03 | Linux | F-003 테스트 실행 UI 개편 — retry 세션 선택 / 커맨드 프리뷰 |
| v0.7.0 | 2026-04-01 | 전체 | F-011 Jira Integration 구현 |
| v0.6.8 | 2026-04-01 | 전체 | F-010 해결방안(Solution) 기능 구현 |
| v0.6.3 | 2026-03-25 | Linux | F-007 대시보드 / F-004 파싱/업로드 초기 구현 |
| v0.5.4 | 2026-03-24 | Linux | `.deb` 설치 패키지 배포 시작 / 자동 업데이트 URL 고정 |
| v0.5.0 | 2026-03-23 | Linux | Suite sub-type, Shard, 디버그 로거, 자동 업데이트 |
| v0.4.0 | 2026-03-23 | Linux | F-001/002/003 구현, PTY 인터랙티브, 결과 요약 감지 |
| v0.1.2 | — | Windows | Windows 배포 초기 버전 |

---

> 상세 개발 이력: [GAH Code Repo](https://github.com/greenhelix/GAH-Code-Repo)
