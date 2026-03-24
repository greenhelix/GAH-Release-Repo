# GAH Linux 설치 가이드

## 시스템 요구사항

- Ubuntu 20.04 LTS 이상 (x64)
- Python 3

## 설치 방법

### .deb 패키지로 설치 (권장)

```bash
sudo dpkg -i gah-linux-amd64.deb

# 의존성 오류 발생 시
sudo apt-get install -f
```

설치 후 앱 메뉴에서 **GAH** 를 실행하거나 터미널에서:
```bash
gah
```

> `/opt/gah/` 에 설치됩니다. 이후 자동 업데이트는 sudo 없이 동작합니다.

---

## 첫 실행 설정

1. **테스트** 탭 → **환경 구축(F-001)** 에서 XTS 경로 설정
   - 예: `/home/user/xts/gts/android-gts-13.1-R2-13-16-14604821`
2. **환경 점검(F-002)** 에서 ADB / Java / SDK 정상 여부 확인
3. **테스트 실행(F-003)** 에서 Suite 선택 후 실행

---

## 필수 환경변수 설정 (`~/.bash_profile`)

XTS 도구 실행 시 `adb`, `aapt`, `APE_API_KEY` 등이 필요합니다.
**`~/.bashrc` 가 아닌 `~/.bash_profile`** 에 추가하세요.

```bash
# Android SDK
export ANDROID_HOME="$HOME/Android"
export PATH="$ANDROID_HOME/platform-tools:$ANDROID_HOME/cmdline-tools/latest/bin:$ANDROID_HOME/build-tools/36.0.0:$PATH"

# GTS 전용
export APE_API_KEY="/path/to/gts-key.json"
```

설정 후:
```bash
source ~/.bash_profile
```

> `~/.bash_profile` 이 없으면 새로 생성하면 됩니다.
> F-003 실행 시 ANDROID_HOME 이 없으면 터미널에 안내 메시지가 표시됩니다.

---

## 디버그 로그

오류 발생 시 아래 경로의 로그 파일을 담당자에게 전달하세요.

```
/opt/gah/logs/gah_YYYYMMDD.log
```

---

## 문제 해결

| 증상 | 해결 방법 |
|------|-----------|
| 의존성 오류 | `sudo apt-get install -f` |
| 화면 미표시 (SSH 환경) | `export DISPLAY=:0` 후 재실행 |
| F-003 즉시 종료 | `~/.bash_profile` 에 `ANDROID_HOME` / `PATH` 설정 확인 |
| adb 인식 안 됨 | `~/.bash_profile` 에 `ANDROID_HOME` 설정 + `source ~/.bash_profile` |
