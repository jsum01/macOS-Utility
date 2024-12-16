# macOS 개발 환경 세팅

## 1. 패키지 매니저
### 1-1. Homebrew
**1-1-1. brew 설치하기**
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
```bash
xcode-select --install
```
```
    echo >> /Users/duit/.zprofile
    echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/duit/.zprofile
    eval "$(/opt/homebrew/bin/brew shellenv)"
```

```bash
 brew install wget
```

### 1-2. Homebrew Cask
앱스토어에 없는 프로그램을 brew를 통해 설치 가능함

그렇다면 cask라는 것은 무엇일까요? 
**1-2-1 cask 설치하기**
```bash
brew install cask
```
**1-2-2 brew cask로 Chrome 설치하기**
```
brew install --cask google-chrome
```

### 1-3. Homebrew mas
**앱스토어**에 있는 프로그램을 brew를 통해 설치 가능함

**1-3-1 mas 설치하기**
```bash
brew install mas
```
**1-3-2 사용법**
```bash
// 아래 명령어를 통해 원하는 패키지를 검색하면 App ID가 뜬다.
mas search kakaotalk

// 아래 명령어를 통해 해당하는 앱을 설치한다.
mas install {App ID}
```

---

## 2. 기기 관리
### 2-1. CPU 상태 확인
RunCat: https://apps.apple.com/kr/app/runcat/id1429033973?mt=12
### 2-2. 배터리 성능 확인 및 관리
**2-2-1 Aldente 설치하기**
```bash
brew install --cask aldente
```
### 2-3. 클리너
**2-3-1 Clean My Mac 설치하기**
```bash
brew install --cask cleanmymac
```

## 3. Mac을 편하게
### 3-1. 단축키 및 키보드 셋업
**3-1-1 HotKey**
  ```
  mas install 975890633
  // 975890633은 mas search hotkey를 했을 때 나오는 HotKey App의 고유번호
  ```
**3-1-2 Karabiner elements**
```
  brew install --cask karabiner-elements
  ```
### 3-2. 터미널
**3-2-1 iterm2**
  ```
  brew install iterm2
  ```
### 3-3. 화면 분할
**3-3-1 Rectangle**
  ```bash
  brew install --cask rectangle
  ```
**3-3-2 Tiles**
  ```bash
  brew install --cask tiles
  ```

---

## 4. Development Environments
### 4-1. IDE
**4-1-1 VSCode**
```bash
brew install --cask visual-studio-code
```

**4-1-2 Intellij**
```bash
brew install --cask intellij-idea
```

**4-1-3 Pycharm**
```bash
brew install --cask pycharm
```
**4-1-4 Android Studio**
```bash
brew install --cask android-studio
```

### 4-2. Framework
**4-2-1 Node.js**
```bash
brew install node
```
**4-2-2 React Native CLI**
```bash
brew install react-native-cli
```
**4-2-3 Flutter SDK**
```bash
brew install --cask flutter
```
### 4-3. Compiler
**4-3-1 gcc/g++**
```bash
brew install gcc
```
### 4-3. Database
**4-3-1 MySQL**
``` 
brew install mysql
```
<img src="https://github.com/user-attachments/assets/56f254fe-4abd-49af-a8a1-69855cecf5f2" alt="brew install mysql">

``` 
brew services start mysql 
```
<img src="https://github.com/user-attachments/assets/142f3251-6bbe-4e5e-8387-baac83435606" alt="brew services start mysql">

``` 
brew services info mysql 
```
<img src="" alt="brew services info mysql">



---

## 터미널 꾸미기

터미널 꾸미기는 잘 정리된 블로그가 너무 많기에 언급만 하겠다.
### 1. zsh, oh-my-zsh 설치 및 셋팅 [링크(클릭)](https://kikit-study.tistory.com/entry/%EB%A7%A5OS-%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD-%EC%85%8B%ED%8C%85%ED%95%98%EA%B8%B0homebrew-zsh-oh-my-zsh-iterm2)

---

## 한 번에 설치하기 - 명령어 모음

### 1. 필수 패키지 및 앱 설치 (Homebrew 기반)

```
# 1. Homebrew 설치
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
xcode-select --install
# 2. Homebrew 기본 패키지 설치
brew install wget gcc mas node react-native-cli
# 3. Homebrew Cask를 이용한 앱 설치
# 설치항목: Google, Iterm2, Rectangle, titles, aldente, cleanMyMac, Visual-Studio-Code, IntelliJ-idea, Pycharm, Android-Studio, Flutter, Karabiner-elements
brew install --cask google-chrome iterm2 rectangle tiles aldente cleanmymac visual-studio-code intellij-idea pycharm android-studio flutter karabiner-elements
```

### 2. 앱스토어 앱 설치 (mas 활용)

```
# 1. mas 설치
brew install mas
# 2. 앱스토어 앱 설치 (예: RunCat, HotKey)
mas install 1429033973 # RunCat
mas install 975890633  # HotKey
```

---

## 기기변경을 했을 때, 데이터 전송은 어떻게 할까?

### [Case 1] Windows to Mac 마이그레이션

    1. Windows와 Mac, 두 기기의 소프트웨어 버전이 모두 최신 버전인지 확인
    2. 동일 Wifi 연결 or LAN 선으로 서로 연결
    3. 디스크 검사를 통해 두 기기 모두 하드 드라이브에 문제가 없는지 확인
       (1) CMD 실행
       (2) `chkdsk` (Enter)
       (3) (2번 과정에서 문제가 있다고 출련된다면) `chkdsk dreve:/c`를 입력해서 해결
    4. [Windows 기기에서] 애플 홈페이지 접속 - Windows용 마이그레이션 프로그램 다운로드
    5. [Mac 기기에서] 첫 설정이라면 마이그레이션 지원이라는 탭이 있어서 쉽게 하시겠지만, 이미 설정 단계를 넘어갔다면 메뉴 - 유틸리티 - 마이그레이션 지원을 실행
    6. 사용가능한 컴퓨터 목록에서 윈도우 PC를 선택 - 동일한 보안 코드가 나오는지 확인한 후 [계속]버튼 클릭
    7. 이동할 데이터 선택(기다림의 시간 ^.^)


### [Case 2] Mac to Mac 마이그레이션

1. 두 Mac이 모두 최신 macOS 버전인지 확인
2. 두 기기를 동일한 네트워크(Wifi or LAN)로 연결
3. [기존 Mac에서] 시스템 설정 → 공유 → "파일 공유" 활성화
4. [새 Mac에서] 초기 설정 진행 시 "마이그레이션 지원" 실행 (이미 설정을 마쳤다면 유틸리티에서 "마이그레이션 지원" 실행)
5. 사용할 네트워크 선택 → 기존 Mac 선택 후 동일 보안 코드 확인 → [계속] 클릭
6. 이동할 데이터 선택 → 이동 시작! (기다림의 미학 필요!)

### [Case 3] 외장 하드 드라이브 활용

1. [기존 기기에서] 외장 하드 드라이브 연결 → 중요한 데이터 복사
2. 외장 드라이브를 새로운 기기에 연결
3. 복사한 데이터를 새 Mac으로 옮기기
   추가적으로, 애플 타임머신 백업 기능을 사용해도 좋음!

### [Case 4] iCLoud에서 내려받기

추천하는 방법은 아니다. 기존 기기에서 iCloud에 올리는 데에도 시간이 오래 걸린다.
심지어 새로운 Mac에서 iCloud로부터 내려받는 것도 한세월이니...
기기를 미리 팔아야 하는 상황이라 iCloud에 백업해놓는 경우가 아니라면 정말 비추천한다.(진짜 느리다...)

## 맥 한/영 전환 딜레이 해결

맥에서는 한/영 전환이 느리다.

왜냐..?
맥에서는 CapsLock이라는 하나의 키가 두 가지 역할을 하기 때문이다.
(한/영 전환, 대문자 전환)

때문에 이 현상을 해결하기 위해서는 따로 설정이 필요하다.

우선, Kanabiner-Elements를 설치한다.
```
brew install karabiner-elements
```

[작성 예정...]
