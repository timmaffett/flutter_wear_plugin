# Flutter Wear Plugin

A plugin that offers Flutter support for Wear OS by Google (Android Wear).

__To use this plugin you must set your `minSdkVersion` to at least `23`.__

## Tutorial

[https://medium.com/flutter-community/flutter-building-wearos-app-fedf0f06d1b4](https://medium.com/flutter-community/flutter-building-wearos-app-fedf0f06d1b4)

## Widgets

There currently two widgets provided by the plugin:

* WatchShape: determines whether the watch is square or round.
* AmbientMode: builder that provides what mode the watch is in. The widget will rebuild whenever the watch changes mode.

## Setup

If you are creating a standalone watch app, add the following to your manifest:

```xml
<application>
  <meta-data
    android:name="com.google.android.wearable.standalone"
    android:value="true"
    />
</application>
```

## Example

Typically, both of those widgets would be used near the root of your app's widget tree:

```dart
class WatchScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return WatchShape(
      builder: (BuildContext context, WearShape shape, Widget? child) {
        return AmbientMode(
          builder: (context, mode, child) {
            return mode == WearMode.active ? ActiveWatchFace() : AmbientWatchFace();
          },
        );
      },
    );
  }
}
```

## Old Requirements

**You DO NOT need to modify these files anymore:**

You can remove all the old wearable references from the previous release. This plugin
automatically adds all required references and settings.

1. `build.gradle`: _wearable dependencies_

2. `AndroidManifest.xml`: _`WAKE_LOCK` and `android.hardware.type.watch`.
   If you are making a standalone app you still need to add the `com.google.android.wearable.standalone`. meta-data
   as indicated above.

3. `MainActivity.kt` or `MainActivity.java`: _all `AmbientMode` references._
