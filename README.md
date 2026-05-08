# GAH Release Repo

Google Auth Helper 설치 파일 배포 전용 저장소.

[![Version Linux](https://img.shields.io/badge/Linux-v1.0.28-blue)](linux/version.json)
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
| Linux | **v1.0.28** | 2026-05-07 |
| Windows | v0.1.2 | 2026-04-28 |
| macOS | v1.0.23 | 2026-05-04 |

---

## 버전 이력

### v1.x

| 버전 | 날짜 | 플랫폼 | 주요 변경 |
|------|------|--------|-----------|
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
