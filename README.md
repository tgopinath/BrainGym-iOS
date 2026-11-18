# Brain Gym for iPhone

A native SwiftUI shell (WKWebView, iOS 17+) around the live web app at https://brain-gym-six.vercel.app, generated from the
[Kolam iOS shell template](https://github.com/tgopinath/kolam-design-system/tree/main/ios/shell-template).
Inside this app the page switches to Apple's Human Interface Guidelines look (Kolam iOS kit: large titles,
Liquid Glass tab bar, back + inline title, haptics); in Safari or any other browser it keeps its own web look.
Web app source: https://github.com/tgopinath/brain-gym

<img src="screenshots/home.jpg" width="200" alt="Home"> <img src="screenshots/games.jpg" width="200" alt="Games"> <img src="screenshots/progress.jpg" width="200" alt="Progress"> <img src="screenshots/rewards.jpg" width="200" alt="Rewards">

## Run it

```sh
xcodebuild -project BrainGym.xcodeproj -scheme BrainGym \
  -destination 'platform=iOS Simulator,name=iPhone 17 Pro' -derivedDataPath build CODE_SIGNING_ALLOWED=NO build
```

Then install `build/Build/Products/Debug-iphonesimulator/BrainGym.app` with `xcrun simctl install booted …`.
Debug builds accept `-KolamStartURL "<url>"` (open another route) and `-KolamJS "<line>"` (run one line of
JavaScript after the first load) on `simctl launch`, for screenshots.
Installing on other people's iPhones needs TestFlight or the App Store (Apple Developer Program).
