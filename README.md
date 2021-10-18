# basic_react_native

## 開発環境
- https://reactnative.dev/docs/environment-setup
  - `React Native CLI Quickstart`のタブを参考にする
  - `Development OS`: macOS
  - `Target OS`: Android

### Node & Watchman
```
brew install node

xcode-select --install
brew install watchman
```

### Java Development Kit
```
brew install --cask adoptopenjdk/openjdk/adoptopenjdk8
```

### Android Studio
- https://developer.android.com/studio

##### `Android SDK`をインストール
- Android Studioを起動し、`Appearance & Behavior` → `System Settings` → `Android SDK`で画面を開く
- `Android 10 (Q)`をチェックし、インストール
- その後、下記を実行

```
sdkmanager "platforms;android-29" "system-images;android-29;default;x86_64" "system-images;android-29;google_apis;x86"
sdkmanager "cmdline-tools;latest" "build-tools;29.0.2"
```

##### `ANDROID_HOME`の環境変数を設定
```
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

### 初期プロジェクトの作成
```
npx react-native init xxxxxx(適切なプロジェクト名をつけてください)
```

##### TypeScriptを利用する場合
```
npx react-native init xxxxxx --template react-native-template-typescript
```

### Genymotionのインストール
- https://www.genymotion.com/download/

##### Virtual Boxのインストール
- https://www.oracle.com/jp/virtualization/technologies/vm/downloads/virtualbox-downloads.html

##### Genymotion起動

- 起動時にエラー
  - `An error has occurred while trying to create a VirtualBox host-only network interface.`
  - こちらのリンクから対応
    - https://support.genymotion.com/hc/en-us/articles/4405183363601--An-error-has-occurred-while-trying-to-create-a-virtualbox-host-only-network-interface-when-launching-Genymotion-Desktop-

## HelloWorldの起動

### Android
```
cd hello_world
yarn
npx react-native start
npx react-native run-android
```

## 参考
- [React Native](https://reactnative.dev/)
