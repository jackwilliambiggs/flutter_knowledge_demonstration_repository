# Flutter Learning Challenges 🐦

This document contains a progressive set of tasks to practice and verify your Flutter fundamentals.  
Each task includes:
- **Goal** → what you should build  
- **Accept** → what counts as “done”  
- **Stretch** → optional extra improvements  

Work through them in order. Each challenge builds on the previous ones.

---

## Level 0 — Setup & Orientation

### 1) Project Bootstrap
- **Goal:** Create a new Flutter app.  
- **Accept:**  
  - `flutter doctor` shows no issues  
  - `flutter run` launches on emulator/device  
  - App title set to your name  
- **Stretch:** Add a custom app icon (Android & iOS).  

### 2) File & Widget Tour
- **Goal:** Explain what `main.dart`, `MaterialApp`, `Scaffold`, and `build` do.  
- **Accept:** `README.md` in repo with short explanations and a diagram of the widget tree.  

---

## Level 1 — Widgets & Layout

### 3) Layout Playground
- **Goal:** Recreate a simple profile card screen.  
- **Accept:** Uses `Column`, `Row`, `Padding`, `SizedBox`, `CircleAvatar`, `Icon`, `Text`.  
- **Stretch:** Extract sub-widgets into separate files (e.g., `ContactRow`, `AvatarHeader`).  

### 4) Lists Two Ways
- **Goal:** Build a scrollable list of 50 items.  
- **Accept:**  
  - One screen uses `ListView(children: [...])`  
  - Another uses `ListView.builder`  
  - Taps show a `SnackBar`  
- **Stretch:** Add pull-to-refresh with `RefreshIndicator`.  

### 5) Images & Assets
- **Goal:** Show a local asset image and a network image with placeholders.  
- **Accept:** Proper `pubspec.yaml` asset config; `Image.asset` and `FadeInImage`.  
- **Stretch:** Add a hero animation between a grid item and a detail page.  

---

## Level 2 — State & Interaction

### 6) Stateful Counter+
- **Goal:** Extend the counter app with increment, decrement, and reset.  
- **Accept:**  
  - Uses `setState`  
  - Disables decrement below 0  
  - Shows current value in AppBar  
- **Stretch:** Persist last value with `shared_preferences`.  

### 7) Forms & Validation
- **Goal:** Create a login form with email & password.  
- **Accept:** Uses `Form`, `TextFormField`, `validator`, `autovalidateMode`, password toggle.  
- **Stretch:** Inline error messages and disabled submit until valid.  

### 8) Navigation Basics
- **Goal:** Two screens: Home → Details with data passed forward and result returned back.  
- **Accept:** Uses `Navigator.push`/`pop`, passes a custom object, receives a boolean result.  
- **Stretch:** Use named routes with `onGenerateRoute`.  

---

## Level 3 — Theming & Adaptation

### 9) Light/Dark Theme Switch
- **Goal:** App-wide theming with a toggle.  
- **Accept:** Custom `ThemeData` for light/dark, toggle updates live.  
- **Stretch:** Use `ThemeExtension` for brand colors.  

### 10) Responsiveness
- **Goal:** Make a dashboard that adapts for phone vs tablet.  
- **Accept:** Uses `LayoutBuilder`/`MediaQuery` to switch layouts.  
- **Stretch:** Use `GridView` with responsive breakpoints.  

---

## Level 4 — Async, Networking & Persistence

### 11) Futures & Streams
- **Goal:** Show a progress indicator while loading a delayed Future, and a live ticking timer via Stream.  
- **Accept:** Uses `FutureBuilder` and `StreamBuilder`.  
- **Stretch:** Add a cancel button for the stream.  

### 12) HTTP Fetch
- **Goal:** Call a public JSON API and display items.  
- **Accept:** Uses `http` package, loading & error states, model class with `fromJson`.  
- **Stretch:** Retry button and pull-to-refresh.  

### 13) Local Persistence
- **Goal:** Save favorite items locally.  
- **Accept:** Use `shared_preferences` or `hive` to persist across restarts.  
- **Stretch:** Add simple filtering & search.  

---

## Level 5 — State Management

### 14) State Management #1 (Provider)
- **Goal:** Lift state out of widgets into a `ChangeNotifier` with `Provider`.  
- **Accept:** Separate data layer; UI rebuilds efficiently.  
- **Stretch:** Add selectors to optimize rebuilds.  

### 15) State Management #2 (Riverpod or Bloc)
- **Goal:** Rebuild the same feature with Riverpod or Bloc/Cubit.  
- **Accept:** Clean separation of concerns; same behavior as Task 14.  
- **Stretch:** Unit test the provider/cubit.  

---

## Level 6 — Animations & Polish

### 16) Implicit & Explicit Animations
- **Goal:** Animate a card expanding/collapsing.  
- **Accept:** One implicit (`AnimatedContainer`) and one explicit (`AnimationController`, `Tween`).  
- **Stretch:** Add a `Hero` transition between list and detail.  

### 17) Accessibility & i18n
- **Goal:** Improve accessibility and add localization.  
- **Accept:** Use `Semantics`, large-text friendly, localize at least 2 strings.  
- **Stretch:** Support RTL (e.g., Arabic) and test mirrored layout.  

---

## Level 7 — Testing & Tooling

### 18) Testing Starter Pack
- **Goal:** Add unit test, widget test, and golden test.  
- **Accept:** `flutter test` passes; golden image generated.  
- **Stretch:** Mock network layer in widget test.  

### 19) Linting & Perf
- **Goal:** Enable `flutter_lints`, fix warnings, run `flutter analyze`.  
- **Accept:** No analyzer issues; use `devtools` to profile and optimize one thing.  
- **Stretch:** Add GitHub Actions CI for tests + analyze.  

---

## Level 8 — Platform & Deployment

### 20) Platform Integrations
- **Goal:** Use a plugin (e.g., `url_launcher`, `path_provider`, camera).  
- **Accept:** Works on Android and iOS; handle permissions gracefully.  
- **Stretch:** Add a platform channel stub that returns a simple string.  

### 21) Packaging & Release (Dry Run)
- **Goal:** Prepare for release builds.  
- **Accept:**  
  - App has name, version, build number  
  - Android release build signed  
  - iOS archive created  
  - Steps documented in README  
- **Stretch:** Add privacy policy page and “About” screen.  

---

## How to Use This
- Make a single repo with folders like `01_setup`, `02_layout`, …  
- Each folder: tiny app or screen + README with **evidence** (screenshots/GIFs).  
- Tick off the **Accept** criteria before moving on.  

---

## Quick Self-Check
- Widgets & layout → Can you sketch a widget tree and explain constraints?  
- State → Do you know when to use `setState` vs Provider/Bloc?  
- Navigation → Can you pass objects and pop with results?  
- Theming → Can you toggle and centralize colors?  
- Async → Can you model loading/error/empty states?  
- Networking → Can you parse JSON and handle errors?  
- Persistence → Can you save and load settings/items?  
- Animations → Can you choose implicit vs explicit?  
- Testing → Can you write unit, widget, and golden tests?  
- Platform → Can you use plugins and permissions?  

---
