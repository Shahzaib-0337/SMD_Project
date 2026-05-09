# Smart Travel Companion

Flutter frontend for the **SMD Final Assignment** theme: explore places (JSONPlaceholder photos), weather (Open‑Meteo), Riverpod state, GoRouter navigation, local cache for offline, and UI aligned with the provided mockups.

## Run

```bash
cd smart_travel_companion
flutter pub get
flutter run
```

Try Chrome: `flutter run -d chrome`

## Build APK

```bash
flutter build apk --release
```

Output: `build/app/outputs/flutter-apk/app-release.apk`

## Stack

- **State:** Riverpod (`Notifier` / `FutureProvider`)
- **Navigation:** GoRouter (`StatefulShellRoute` + full-screen `/detail`, `/search`)
- **APIs:** `https://jsonplaceholder.typicode.com/photos` (paginated), Open‑Meteo forecast
- **Persistence:** `shared_preferences` (favorites, theme, recents), file cache (mobile/desktop) for places JSON

## Rubric mapping (high level)

| Area | What we implemented |
|------|---------------------|
| Architecture | `lib/core`, `lib/data`, `lib/models`, `lib/providers`, `lib/presentation` |
| APIs + errors | Repositories, retry UI, empty search state, offline/cached banner |
| Animations | `AnimatedList` (home), `Hero` (images), `AnimatedSize` + `AnimatedRotation` (about), `AnimatedSwitcher` (weather), `AnimatedContainer` / `AnimatedOpacity` (chips, banner) |
| UI/UX | Drawer, bottom app bar + FAB, cards, weather panel, dark mode |
| Offline | Cache on successful fetch; offline path reads cache |


