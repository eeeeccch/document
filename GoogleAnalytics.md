### Android Debug Brige
```shell
brew install android-platform-tools
```

### Google Analytics DebugView 보고서 연동
```shell
adb shell setprop debug.firebase.analytics.app {package name}
```

### Command log view
```shell
adb logcat -v time -s FA FA-SVC
```
