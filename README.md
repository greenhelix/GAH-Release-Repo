# GAH Release Repo

Google Auth Helper 설치 파일만 보관하는 릴리즈 전용 저장소입니다.

## 저장소 구성

```text
linux/
  INSTALL.md          ← 설치 가이드 (공통)
  version.json        ← 자동 업데이트용 최신 버전 정보
  vX.Y.Z/
    gah-vX.Y.Z-linux-x64.tar.gz

windows/
  vX.Y.Z/
    gah-windows-vX.Y.Z-setup.exe
```

## 설치 방법

**Linux (Ubuntu)**
- `linux/INSTALL.md` 를 먼저 읽고 설치합니다.

**Windows**
- `windows/<version>/` 폴더의 `.exe` 설치 파일을 실행합니다.

---

## 버전 이력

### `v0.5.3` (2026-03-24) — Linux
- 앱 아이콘 변경: 파란 계열 방패+체크 디자인
- F-003: 터미널 입력창 항상 표시 (실행 중 활성 / 미실행 시 비활성)
- 디버그 로그 경로 변경: `{bundle}/logs/gah_YYYYMMDD.log`
- XTS 도구 실행 시 `/bin/bash -l` 로그인 셸 적용 (`.bash_profile` PATH 상속)

### `v0.5.2` (2026-03-24) — Linux
- F-003: Suite 드롭다운에 `(직접 실행)` 항목 추가
- F-002/003: `adb` / `sdkmanager` 전체 경로 직접 실행으로 인식 수정
- 디버그 로거 강화: 경로 해석 / retry 결정 / 빠른 종료 감지 로깅 추가

### `v0.5.1` (2026-03-23) — Linux
- F-002: adb/sdkmanager 환경 점검 인식 수정 (로그인 셸 경유)
- 설정 페이지: 앱 버전 표시, 디버그 로그 경로 클립보드 복사 버튼 추가

### `v0.5.0` (2026-03-23) — Linux
- F-003: Suite sub-type 드롭다운, Shard 기능, 자동 재시도 모드
- Core: 앱 디버그 로거, GitHub 자동 업데이트 기능

### `v0.4.0` (2026-03-23) — Linux
- F-001/002/003 기능 구현 (XTS 경로 설정, 환경 점검, 테스트 실행)
- PTY 인터랙티브 모드, 결과 요약 감지 (PASS/FAIL/Total)

### `v0.1.2` — Windows
- Windows 자동 테스트 메뉴 비활성화
- 우측 상단 플랫폼 아이콘 포커스 가시성 개선

---

## 메모

- 상세 개발 내용은 코드 저장소에서 관리합니다.
- 이 저장소는 설치용 결과물 배포와 버전 이력 확인 용도로만 사용합니다.
