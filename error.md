#  报错问题记录

### 1.Unable to determine activity name

最新的Android Studio长颈鹿版（Android Studio Giraffe | 2022.3.1 Patch 4）好像对Java不太友好，强推科特林语言。如果新建一个空白的Activity，好像只能选科特林，然尔如果选No Activity，则可以选Java语言。前提新建好后，不像以前的老版本，点击运行，可以直接进入Hello world。这里至少还缺少两个东西：一是新建一个空白Activity，里面自己写一个“Hello world!”；二是在mainfest里，添加点内容：

```xml
<activity
    android:name=".MainActivity"
    android:exported="true"
    android:theme="@style/Theme.AppCompat.DayNight">
    <intent-filter>
        <action android:name="android.intent.action.MAIN" />

        <category android:name="android.intent.category.LAUNCHER" />
    </intent-filter>
</activity>
```