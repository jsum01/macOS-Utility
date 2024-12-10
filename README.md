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


## 내 맥에 한 번에 다 설치하기
<aside>
 이 명령어는 오롯이 필자의 환경 셋팅을 한 번에 하기 위한 명령어 모음집입니다.
</aside>
