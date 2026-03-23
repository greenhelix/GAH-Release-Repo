# GAH Release Repo

Google Auth Helper 설치 파일만 보관하는 릴리즈 전용 저장소입니다.

## 저장소 구성

이 저장소에는 플랫폼별 설치 파일과 간단한 설치 안내만 포함합니다.

```text
windows/
  vX.Y.Z/
    gah-windows-vX.Y.Z-setup.exe
    INSTALL.txt

linux/
  vX.Y.Z/
    gah-vX.Y.Z-linux-x64.tar.gz
    INSTALL.txt
```

## 사용 방법

**Windows**
- `windows/<version>/` 폴더에서 설치 파일과 `INSTALL.txt` 를 확인합니다.

**Linux (Ubuntu)**
- `linux/<version>/` 폴더에서 `INSTALL.txt`를 먼저 읽고 설치합니다.

## 최신 배포

- `v0.4.0` (2026-03-23) — Linux
  - F-001/002/003 기능 구현 (XTS 경로 설정, 환경 점검, 테스트 실행)
  - 자동 재시도, PTY 인터랙티브 모드, 결과 요약 감지
  - 앱 디버그 로그 자동 저장 (`~/gah_debug_YYYYMMDD.log`)

- `v0.1.2` — Windows
  - Windows 자동 테스트 메뉴 비활성화
  - 우측 상단 플랫폼 아이콘 포커스 가시성 개선
  - 데스크톱 릴리즈 산출물 단순화

## 메모

- 상세 개발 내용은 코드 저장소에서 관리합니다.
- 이 저장소는 설치용 결과물 배포와 버전 이력 확인 용도로만 사용합니다.
