---
layout: single
title:  "Windows에서 wsl을 실수로 두 개 설치했을 때 하나를 지우려면?"
---

# 하나 끄고 24.04만 쓰려면??
```
PS C:\Users\devra> wsl -l -v
  NAME            STATE           VERSION
* Ubuntu          Running         2
  Ubuntu-24.04    Running         2
```

현재 WSL에서 두 개의 인스턴스(`Ubuntu`와 `Ubuntu-24.04`)가 실행 중입니다. 하나(예: `Ubuntu`)를 종료하고 `Ubuntu-24.04`만 실행하려면 다음 단계를 따르세요.

---

### **1. 현재 실행 중인 WSL 상태 확인**
```bash
wsl -l -v
```
출력:
```
  NAME            STATE           VERSION
* Ubuntu          Running         2
  Ubuntu-24.04    Running         2
```

여기서 `*` 표시된 `Ubuntu`가 기본 인스턴스이며, 두 인스턴스가 모두 실행 중입니다.

---

### **2. 특정 WSL 인스턴스 종료**
`Ubuntu`를 종료하려면 다음 명령을 사용합니다:

```bash
wsl --terminate Ubuntu
```

#### 확인:
```bash
wsl -l -v
```
출력:
```
  NAME            STATE           VERSION
  Ubuntu          Stopped         2
* Ubuntu-24.04    Running         2
```

이제 `Ubuntu-24.04`만 실행 중입니다.

---

### **3. 기본 WSL 인스턴스 설정**
현재 기본 인스턴스는 `Ubuntu`로 설정되어 있습니다. `Ubuntu-24.04`를 기본으로 설정하려면 다음 명령을 실행하세요:

```bash
wsl --set-default Ubuntu-24.04
```

#### 확인:
```bash
wsl -l -v
```
출력:
```
  NAME            STATE           VERSION
  Ubuntu          Stopped         2
* Ubuntu-24.04    Running         2
```

`*` 표시가 `Ubuntu-24.04`로 이동했음을 확인할 수 있습니다.

---

### **4. 기본 WSL 인스턴스를 사용해 새 터미널 열기**
이제 새 WSL 터미널을 열면 자동으로 `Ubuntu-24.04`가 실행됩니다.

---

### **추가 정보**
- 특정 인스턴스를 시작하려면:
  ```bash
  wsl -d Ubuntu-24.04
  ```
- WSL에서 특정 인스턴스를 삭제하려면:
  ```bash
  wsl --unregister Ubuntu
  ```
  **주의:** 이 명령은 해당 인스턴스를 완전히 삭제합니다(데이터 포함). 삭제 전에 필요한 데이터를 백업하세요.

---

이 방법으로 `Ubuntu-24.04`만 실행하도록 설정할 수 있습니다.😊
