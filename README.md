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

```bash
 brew install wget
```

### 1-2. Homebrew Cask
앱스토어에 없는 프로그램을 brew를 통해 설치 가능함

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

## 5. 기기변경을 했을 때, 데이터 전송은 어떻게 할까?

### Windows to Mac 마이그레이션

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


### Mac to Mac 마이그레이션

1. 두 Mac이 모두 최신 macOS 버전인지 확인
2. 두 기기를 동일한 네트워크(Wifi or LAN)로 연결
3. [기존 Mac에서] 시스템 설정 → 공유 → "파일 공유" 활성화
4. [새 Mac에서] 초기 설정 진행 시 "마이그레이션 지원" 실행 (이미 설정을 마쳤다면 유틸리티에서 "마이그레이션 지원" 실행)
5. 사용할 네트워크 선택 → 기존 Mac 선택 후 동일 보안 코드 확인 → [계속] 클릭
6. 이동할 데이터 선택 → 이동 시작! (기다림의 미학 필요!)

### 외장 하드 드라이브 활용

1. [기존 기기에서] 외장 하드 드라이브 연결 → 중요한 데이터 복사
2. 외장 드라이브를 새로운 기기에 연결
3. 복사한 데이터를 새 Mac으로 옮기기
   추가적으로, 애플 타임머신 백업 기능을 사용해도 좋음!

### iCLoud에서 내려받기

추천하는 방법은 아니다. 기존 기기에서 iCloud에 올리는 데에도 시간이 오래 걸린다.
심지어 새로운 Mac에서 iCloud로부터 내려받는 것도 한세월이니...
기기를 미리 팔아야 하는 상황이라 iCloud에 백업해놓는 경우가 아니라면 정말 비추천한다.(진짜 느리다...)
