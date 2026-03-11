# GAH Release Repo

Google Auth Helper 설치 파일만 보관하는 릴리즈 전용 저장소입니다.

## 저장소 구성

이 저장소에는 플랫폼별 설치 파일과 간단한 설치 안내만 포함합니다.

```text
windows/
  vX.Y.Z/
    gah-windows-vX.Y.Z-setup.exe
    INSTALL.txt

ubuntu/
  vX.Y.Z/
    gah-ubuntu-vX.Y.Z.deb
    INSTALL.txt
```

## 사용 방법

Windows
- `windows/<version>/` 폴더에서 설치 파일과 `INSTALL.txt` 를 확인합니다.

Ubuntu
- `ubuntu/<version>/` 폴더에서 설치 파일과 `INSTALL.txt` 를 확인합니다.

## 최신 배포

- `v0.1.2`
  - Windows 자동 테스트 메뉴 비활성화
  - 우측 상단 플랫폼 아이콘 포커스 가시성 개선
  - 데스크톱 릴리즈 산출물 단순화

## 메모

- 상세 개발 내용은 코드 저장소에서 관리합니다.
- 이 저장소는 설치용 결과물 배포와 버전 이력 확인 용도로만 사용합니다.
