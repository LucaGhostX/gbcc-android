# [GBCC Android](https://gbcc.github.io)
This is the android front-end to [GBCC](https://gbcc.github.io), a
cross-platform Game Boy and Game Boy Color emulator written in C with a focus
on accuracy. See the [main repository](https://github.com/philj56/gbcc) for
details.

## Fork New Features (Vide-coded)
This fork includes several improvements and new features implemented via AI assistance (vide-coded):

### Camera and Sensors
- **CameraX Integration**: Full migration and implementation of CameraX APIs for modern and performant camera management.
- **Rapid Sensor Switching**: Added a touch button to cycle between front and back cameras directly during emulation.
- **A + Photo Combo Button**: A new dedicated button that emulates the Game Boy 'A' key while simultaneously capturing a high-resolution photo with the smartphone sensor.

### Printer
- **Automatic Cropping**: Images exported via the Printer function are now automatically cropped (16 pixels at the top and 48 pixels at the bottom) to eliminate unwanted margins.

### Interface and Customization
- **New GBC Colors**: Added new shell color options for the Game Boy Color, including Atomic Purple, Glacier, Red, Blue, Orange, and an Yellow.
- **Enhanced Touch Controls**:
    - Real text overlays (TextView) on A, B, START, and SELECT buttons using the `sans-serif-black` system font for maximum sharpness.
    - Full integration of the new Camera buttons into the "Rearrange layout" feature, with drag-and-drop support and resizing via a dedicated slider.
    - Dynamic UI adaptation: the A + Photo button automatically turns blue when using Red or Berry skins to ensure visibility.
- **Layout Optimizations**: Added ScrollView to the layout customization screen and fixed various icon and slider overlap issues.

## Install
### From source
I'll write up instructions on this at some point, but it's pretty much just
install the Android SDK & NDK, clone this repo recursively, and then run

```sh
./gradlew build
```

This will generate the apks in `app/build/outputs/apk/`.

~~You can get gbcc on Google Play.~~

~~### Prebuilt packages !~~

~~Debug packages are generated on each commit. To download them, navigate to the
actions tab (you'll need to be logged in to GitHub to do this). Select the latest "Build Packages" job that
succeeded, and look for the artifacts dropdown.~~

---
## *Disclaimer: These modifications were made for my own personal use. I take neither credit nor responsibility for the original work or for the modifications made, and they are provided as-is.*
