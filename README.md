# GAH Release Repo

Google Auth Helper 설치 파일만 보관하는 릴리즈 전용 저장소입니다.

## 저장소 구성

```text
linux/
  gah-linux-amd64.deb     ← 최초 설치용 (항상 최신)
  gah-linux-x64.tar.gz    ← 자동 업데이트용 (항상 최신)
  version.json            ← 앱 내 자동 업데이트 메타데이터
  INSTALL.md              ← 설치 가이드

windows/
  v0.1.2/
    gah-windows-v0.1.2-setup.exe
```

## 설치 방법

**Linux (Ubuntu)**
```bash
sudo dpkg -i gah-linux-amd64.deb
```
→ 자세한 내용: `linux/INSTALL.md`

**업데이트**
앱 실행 시 자동으로 신버전 감지 → `gah-linux-x64.tar.gz` 다운로드 후 적용

---

## 버전 이력

### `v0.5.4` (2026-03-24) — Linux
- F-003: ANDROID_HOME 미설정 시 터미널에 설정 안내 출력
- F-003: 2초 미만 종료 시 `.bash_profile` 확인 안내 출력
- 앱 시작 로그에 `.bash_profile` 존재 여부 추가
- Linux `.deb` 설치 패키지 지원 시작 (`/opt/gah/` 설치, 앱 메뉴 등록)
- 자동 업데이트 URL 고정 경로로 변경 (버전 폴더 제거)

### `v0.5.3` (2026-03-24) — Linux
- 앱 아이콘 변경: 파란 계열 방패+체크 디자인
- F-003: 터미널 입력창 항상 표시 (실행 중 활성 / 미실행 시 비활성)
- 디버그 로그 경로: `{bundle}/logs/gah_YYYYMMDD.log`
- XTS 도구 실행 시 `/bin/bash -l` 적용 (`.bash_profile` PATH 상속)

### `v0.5.2` (2026-03-24) — Linux
- F-003: Suite 드롭다운에 `(직접 실행)` 항목 추가
- F-002/003: `adb` / `sdkmanager` 전체 경로 직접 실행으로 인식 수정
- 디버그 로거 강화

### `v0.5.1` (2026-03-23) — Linux
- F-002: adb/sdkmanager 환경 점검 인식 수정
- 설정 페이지: 앱 버전 표시, 디버그 로그 경로 클립보드 복사

### `v0.5.0` (2026-03-23) — Linux
- F-003: Suite sub-type, Shard, 자동 재시도 모드
- Core: 디버그 로거, GitHub 자동 업데이트

### `v0.4.0` (2026-03-23) — Linux
- F-001/002/003 기능 구현 (경로 설정, 환경 점검, 테스트 실행)
- PTY 인터랙티브 모드, 결과 요약 감지

### `v0.1.2` — Windows
- Windows 자동 테스트 메뉴 비활성화

---

## 메모

- 상세 개발 내용은 코드 저장소에서 관리합니다.
- 이 저장소는 설치용 결과물 배포와 버전 이력 확인 용도로만 사용합니다.
