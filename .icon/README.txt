App icon set
============

iOS
---
Drag AppIcon.appiconset into Assets.xcassets in Xcode,
replacing the existing set. Contents.json is included.

Transparency has been flattened onto the background colour:
App Store validation rejects icons with an alpha channel.
Corners are square on purpose - iOS applies its own mask.

Android
-------
Copy the res folder into app/src/main/ and let it merge with
the existing res folder. The <application> element in
AndroidManifest.xml should use:
  android:icon="@mipmap/ic_launcher"
  android:roundIcon="@mipmap/ic_launcher_round"

Android 8 and later: mipmap-anydpi-v26/ic_launcher.xml places
ic_launcher_foreground.png (72 dp logo on a 108 dp layer) on the
colour in values/ic_launcher_background.xml.
ic_launcher_monochrome.png is the Android 13+ themed icon layer:
only its transparency is used, the system supplies the colour.
Android 7 and older: ic_launcher.png and ic_launcher_round.png.

Newer Android Studio templates also have res/mipmap-anydpi/ic_launcher.xml.
Delete it so the project has a single icon definition.

play-store-512.png is for the Play Console listing, not the app.
