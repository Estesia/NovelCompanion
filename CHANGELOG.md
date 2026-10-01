# Changelog

All notable changes to **NovelCompanion** are documented here.

This project is still in active development, so milestone names and internal architecture may continue to evolve.

## Unreleased

### Added
- Ongoing integration work between the AI worker layer, orchestration, and persistent project data.
- Continued refinement of the Android-facing build path and project structure.

### Changed
- Repository documentation is being normalized so build inputs, architecture notes, and project history are easier to follow.

## 2026-09 — Initial repository build workflow

### Added
- Android project source package: `NovelCompanion_Vivi_Android.zip`.
- GitHub Actions workflow for unpacking the Android source and building a debug APK.
- JDK 17, Android SDK 35, and Gradle 8.7 CI setup.
- GitHub Actions artifact upload for generated debug APKs.

### Notes
- The ZIP-based source layout is a milestone packaging choice, not the intended permanent repository structure.
