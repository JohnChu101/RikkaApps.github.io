### 关于从 Android 9 引入的 hidden API 限制

App Ops 必须使用一些隐藏 API，但从 Android 9 开始普通应用不能使用。

为了使用 App Ops，你需要关闭这个限制，使用 adb

```
adb shell
settings put global hidden_api_blacklist_exemptions \*
```

或使用任意终端应用（如果设备已 root）

```
su
settings put global hidden_api_blacklist_exemptions \*
```

做完后，你需要强行停止 App Ops 设置重启设备。

如果此问题仍然存在，请联系我们。

#### 特别提示

MIUI （可能还有其他 ROM）默认不允许 adb 修改系统设置，你需要在系统的“开发者选项”中开启“USB 调试（安全选项）”或类似选项。