# GAH Linux 설치 가이드

## 시스템 요구사항

- Ubuntu 20.04 LTS 이상 (x64)
- ADB, Java 11+, Python 3

## 의존 패키지 설치

```bash
sudo apt-get install -y libgtk-3-0 libblkid1 liblzma5 \
    libglib2.0-0 adb openjdk-17-jdk python3
```

## 설치 및 실행

```bash
tar -xzf gah-vX.Y.Z-linux-x64.tar.gz
./gah
```

> `tar` 압축 해제 시 현재 디렉토리에 번들 파일이 풀립니다. 별도 폴더를 만들어 그 안에서 해제하는 것을 권장합니다.

## 첫 실행 설정

1. 앱 실행 후 **테스트** 탭 이동
2. **환경 구축(F-001)** 에서 XTS 경로 설정
   - 예: `/home/user/xts/gts/android-gts-13.1-R2-13-16-14604821`
3. **환경 점검(F-002)** 에서 ADB / Java / SDK 정상 여부 확인
4. **테스트 실행(F-003)** 에서 Suite 선택 후 실행

## 환경변수 설정 (`~/.bash_profile`)

XTS 도구가 `adb`, `aapt`, `APE_API_KEY` 등을 필요로 합니다.
`~/.bashrc` 가 아닌 **`~/.bash_profile`** 에 아래 내용을 추가하세요.

```bash
export ANDROID_HOME="$HOME/Android"
export PATH="$ANDROID_HOME/platform-tools:$ANDROID_HOME/cmdline-tools/latest/bin:$ANDROID_HOME/build-tools/36.0.0:$PATH"
export APE_API_KEY="/path/to/key.json"   # GTS 전용
```

## 디버그 로그

오류 발생 시 아래 경로의 로그 파일을 담당자에게 전달합니다.

```
{gah 실행 파일 위치}/logs/gah_YYYYMMDD.log
```

## 문제 해결

| 증상 | 해결 방법 |
|------|-----------|
| 화면 미표시 (SSH 환경) | `export DISPLAY=:0` 후 재실행 |
| 의존성 오류 | `sudo apt-get install -f` |
| adb 인식 안 됨 | `~/.bash_profile` 에 `ANDROID_HOME` 설정 확인 |
| XTS 실행 오류 (adb/aapt not found) | `~/.bash_profile` 에 `PATH` 및 `APE_API_KEY` 설정 확인 |
