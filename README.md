# Xylophone

Turn your iPhone or iPad into a colourful musical instrument and learn the basics of sound playback with **AVFoundation**.

---

## About

**Xylophone** is a single‑view iOS app written in **Swift 5** that demonstrates how to play short audio clips on‑demand. It is adapted from the App Brewery’s *Complete iOS Development Bootcamp* “Xylophone‑iOS13” module but cleaned up and modernized for Xcode 15 and iOS 17. 🙌

## Features

|    | Capability                                        |
| -- | ------------------------------------------------- |
| 🎵 | Seven colour‑coded keys mapped to the notes C – B |
| ⚡️ | Instant playback using `AVAudioPlayer`            |
| 📳 | Optional haptic feedback on key press             |
| 🎨 | Auto‑layout & Dynamic Type friendly UI            |
| 🛠 | 100 % Swift—no external dependencies              |


## Project Structure

```
Xylophone-iOS13/
├─ Xylophone.xcodeproj          # Xcode project
└─ Xylophone/                   # Source files
   ├─ AppDelegate.swift
   ├─ ViewController.swift      # Main view logic
   ├─ Assets.xcassets/          # App icons + colours
   ├─ Storyboard/
   │  ├─ Main.storyboard
   │  └─ LaunchScreen.storyboard
   └─ Resources/
      └─ Sounds/*.wav           # 7 note samples
```

> *File names may differ slightly—use this as a high‑level guide.*

## How It Works

1. Each key button triggers `@IBAction keyPressed(_:)` in **`ViewController.swift`**.
2. The method looks up the corresponding `.wav` file in the **app bundle** and initialises `AVAudioPlayer` with it.
3. The player is stored on a property to remain in memory for the duration of the sound and `play()` is called.
   This pattern is recommended by Apple and countless iOS devs on Stack Overflow.
   (See Apple docs *Using Audio* and the App Brewery tutorial.)
4. The button’s alpha is briefly lowered for a pressed‑state animation.
5. If **Haptics** are available, a light impact feedback is generated.



## License

Distributed under the MIT License. See **LICENSE** for more information.

---

> **Credits**
>
> Adapted from the [App Brewery Xylophone‑iOS13 tutorial](https://github.com/appbrewery/Xylophone-iOS13). Thanks to Angela Yu for the original inspiration.
