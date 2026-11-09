# Mobile Engineer

**Role:** builds apps for phones and tablets on Android, iOS or a cross-platform framework.
**Prerequisites:** [Programming basics](../1-basics/programming-basics.md). Pick one platform first.

## Skills, in order
1. A platform language: Kotlin or Swift
2. UI toolkit: Jetpack Compose or SwiftUI
3. App lifecycle, navigation and state
4. Networking and local storage
5. Permissions, privacy and security basics
6. Testing and debugging on devices
7. Publishing and release management

**Path at a glance:**
- Android: Android Basics with Compose, then Kotlin docs.
- iOS: Develop in Swift tutorials, then Stanford CS193p.
- Cross-platform: Flutter or React Native, once you know one native platform.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [Android Basics with Compose](https://developer.android.com/courses/android-basics-compose/course) | Beginner | Free | Official Google course with codelabs. Check the current course name. | Build and run a simple Android app with Compose. |
| [Kotlin documentation](https://kotlinlang.org/docs/home.html) | Beginner to Intermediate | Free | Official docs and Kotlin Koans-style exercises. | Write idiomatic Kotlin with coroutines. |
| [Android Developers: Jetpack Compose](https://developer.android.com/develop/ui/compose) | Intermediate | Free | Official tutorials and guides. | Build stateful, themed UIs and navigate between screens. |
| [Develop in Swift tutorials](https://developer.apple.com/tutorials/develop-in-swift/) | Beginner | Free | Apple's guided tutorials for Swift and SwiftUI. A Mac with Xcode is required. | Build a first iOS app with SwiftUI. |
| [Stanford CS193p](https://cs193p.sites.stanford.edu) | Intermediate | Free | Stanford lectures on SwiftUI app development. Check the current edition. | Design apps with MVVM, state and animations. |
| [Flutter documentation and codelabs](https://docs.flutter.dev) | Beginner to Intermediate | Free | Official docs, codelabs and sample apps for a cross-platform toolkit. | Build one app for Android and iOS from a Dart codebase. |
| [React Native documentation](https://reactnative.dev/docs/getting-started) | Intermediate | Free | Official docs for cross-platform apps in React. Pairs well with [Frontend Engineer](frontend-engineer.md). | Reuse React skills to ship mobile apps. |
| [OWASP MASVS](https://mas.owasp.org/MASVS/) | Intermediate to Advanced | Free | Supplementary: mobile application security standard with a testing guide. See [cybersecurity](../../cybersecurity/README.md). | Check an app against recognized mobile security requirements. |

## Certifications
Associate Android Developer certification is no longer offered, so rely on a published app. Verify current options.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder.

1. **Core app** (Beginner, ~1 week)
   - **Build:** a multi-screen app with a list, a detail screen, navigation and state that survives rotation or relaunch.
   - **Practice:** platform language, UI toolkit, lifecycle, navigation.
   - **Done when:** the app runs on an emulator and a real device, and state survives lifecycle changes.
2. **Data and offline** (Intermediate, ~1 week)
   - **Build:** fetch from a public API, cache in local storage and show cached data offline, with clear loading, empty and error states.
   - **Practice:** networking, local storage, state handling.
   - **Done when:** the app works in airplane mode with data from the last sync.
3. **Quality and release** (Intermediate, ~1 week)
   - **Build:** permissions handled correctly, secure storage for tokens, unit and UI tests, a profiling pass and a signed release build.
   - **Practice:** privacy, testing, debugging, release management.
   - **Done when:** tests pass, a profile shows no obvious jank, and a release build installs on a device.

### Final project
**Time:** 3 to 4 weeks. An offline-first app with at least four screens and a real use case, ready for a test track.

**Specific to this project:**
- Safe handling of tokens and user data, with a short privacy note.
- CI that builds and tests on every pull request.
- Crash and error handling, with logs you can use to diagnose a failure.
- A signed release build and store-listing materials (description, screenshots, privacy notes).

Also meets the [production-like bar](../../README.md#what-production-like-means).
