# Repository Structure

NovelCompanion is currently in a transitional repository layout.

## Current layout

```text
NovelCompanion/
├─ .github/
│  └─ workflows/
│     └─ build-apk-from-zip.yml
├─ docs/
│  └─ REPOSITORY_STRUCTURE.md
├─ CHANGELOG.md
├─ README.md
├─ .gitignore
└─ NovelCompanion_Vivi_Android.zip
```

## Why the Android source is still a ZIP

The current GitHub Actions workflow expects `NovelCompanion_Vivi_Android.zip` at the repository root, extracts it into a temporary build directory, and compiles the debug APK from there.

Moving or unpacking that archive now would change the build contract. For that reason, the repository is being cleaned up around the existing build first instead of breaking a working pipeline for cosmetic reasons.

## Intended direction

When the Android source is ready to become the canonical repository layout, the preferred migration is:

```text
NovelCompanion/
├─ .github/workflows/
├─ app/
├─ gradle/
├─ docs/
├─ CHANGELOG.md
├─ README.md
├─ build.gradle(.kts)
├─ settings.gradle(.kts)
└─ gradlew / gradlew.bat
```

At that point the CI workflow should build directly from the checked-in Android project and the ZIP milestone package can be retained only as a historical release asset if still useful.
