
# 2.0.0

- Kotlin ot 1.8.10
- merged AmbientWidget onUpdate(WearMode) change [PR 17](https://github.com/fluttercommunity/flutter_wear_plugin/pull/17)
   (this is a breaking change to version number to 2.0.0)
- added namespace to adroid/build.gradle [PR 27](https://github.com/fluttercommunity/flutter_wear_plugin/pull/27)
- added proguard config so ambient works in release mode [PR 24](https://github.com/fluttercommunity/flutter_wear_plugin/pull/24)
- fixed enum name to WearMode in README.md [PR 28](https://github.com/fluttercommunity/flutter_wear_plugin/pull/28) or
      [PR 31](https://github.com/fluttercommunity/flutter_wear_plugin/pull/31) (both same change)
- fix README.md to refer to correct number of widgets [PR 23](https://github.com/fluttercommunity/flutter_wear_plugin/pull/23)
- No longer include standalone app directive in `android/src/main/AndroidManifest.xml', update readme to direct users
  to add this directive if they need it [PR 22](https://github.com/fluttercommunity/flutter_wear_plugin/pull/22)

# 1.1.0

- Fix issue with non-windows builds breaking.

# 1.0.0

- Null Safety Migration (Finally!)
  - Thanks to Rexios and Peter Ullrich.
  - Min Dart 2.12 / Flutter 2.5
- Updated native component versions:
  - Gradle 6.5
  - Android Gradle Plugin 4.1.0
  - Android compileSdkVersion 31
  - AndroidX Wear 1.2.0
  - Kotlin 1.5.10
  - Removed `jcenter()` repo requirement.

# 0.1.1

- Fix Kotlin/Android compileOnly dep on com.google.android.wearable:wearable.

# 0.1.0

- Updated to AndroidX and Android embedding v2.
- Renamed `Shape` is now `WearShape`.
- Renamed `Mode` is now `WearMode`.
- Deprecated `InheritedShape`.
  _Add `WatchShape` instead and use `WatchShape.of(context)` to get the shape value._

# 0.0.1

- Initial release
