# macOS 개발 환경 세팅

## 패키지 매니저
### 1. Homebrew
1-1. brew 설치하기
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
```bash
xcode-select --install
```

```bash
 brew install wget
```

### 2. Homebrew Cask
앱스토어에 없는 프로그램을 brew를 통해 설치 가능함
2-1 cask 설치하기
```bash
brew install cask
```
2-2 brew cask로 Chrome 설치하기
```
brew install --cask google-chrome
```

### 3. Homebrew mas
앱스토어에 있는 프로그램을 brew를 통해 설치 가능함
3-1 mas 설치하기
```bash
brew install mas
```
3-2 사용법
```bash
// 아래 명령어를 통해 원하는 패키지를 검색하면 App ID가 뜬다.
mas search kakaotalk

// 아래 명령어를 통해 해당하는 앱을 설치한다.
mas install {App ID}
```

## 기기 관리
### CPU 상태 확인
RunCat: https://apps.apple.com/kr/app/runcat/id1429033973?mt=12
### 배터리 성능 확인 및 관리
Aldente
```bash
brew install --cask aldente
```
### 클리너
Clean My Mac
```bash
brew install --cask cleanmymac
```


## 화면 분할
Rectangle
  ```bash
  brew install --cask rectangle
  ```
Tiles
  ```bash
  brew install --cask tiles
  ```

## IDE
VSCode
```bash
brew install --cask visual-studio-code
```

Intellij
```bash
brew install --cask intellij-idea
```

Pycharm
```bash
brew install --cask pycharm
```
Android Studio
```bash
brew install --cask android-studio
```

### Framework
Node.js
```bash
brew install node
```
React Native CLI
```bash
brew install react-native-cli
```
Flutter SDK
```bash
brew install --cask flutter
```
### Compiler
gcc/g++
```bash
brew install gcc
```
