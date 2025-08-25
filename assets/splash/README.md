# Weather App Splash Assets

Two scalable SVG splash screens for a weather app.

- splash-light.svg: sunny + clouds + raindrops
- splash-dark.svg: night crescent + clouds + raindrops

## Preview locally
- Open `assets/splash/preview.html` in a browser
- Toggle light/dark, download SVG directly

## Customize
- Colors: Edit gradients `bgLight`, `bgDark`, `sunGrad`, `dropGrad`
- Sun/Moon: tweak `<circle cx cy r>`
- Cloud: edit the single `<path>` with `filter="url(#shadowSoft)"`
- Raindrops: duplicate/remove the three drop `<path>` elements

## Integration quick notes

### iOS
- In Xcode, add images to `Assets.xcassets` (light/dark variations)
- Export PNGs at 1024, 2048, 3072 px for 1x/2x/3x
- Use in Launch Screen storyboard/SwiftUI; set interface style to Automatic

### Android
- Export PNGs for mipmap: 1024, 800, 600, 400, 200 px (xxxhdpi→mdpi)
- Android 12+: set `windowSplashScreenBackground` and `windowSplashScreenAnimatedIcon`

### React Native / Expo
- Expo: set `expo.splash` in `app.json` (+ `userInterfaceStyle: automatic`)
- RN: use `react-native-bootsplash` or native launch screen

### Web (PWA)
- Include `maskable` and `any` icons in `manifest.json`
- Prefer SVG, provide PNG fallbacks

## Exporting PNGs
- Inkscape/Illustrator: open SVG → Export PNG → set size (square) → export

License: Use freely. Attribution appreciated but not required.