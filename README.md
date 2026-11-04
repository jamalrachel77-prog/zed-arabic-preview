# Zed Arabic Preview

This repository is a **build recipe** for an experimental Arabic-localization patch over the official Zed source tree. It is not a fork of Zed.

## What it does

- Checks out the official `zed-industries/zed` source at the upstream commit pinned in the workflow.
- Applies the Arabic patch stored under `patches/`.
- Builds the Windows x64 Zed executable on a GitHub-hosted Windows runner.
- Publishes the resulting executable as a downloadable GitHub Actions artifact.

## Run the build

1. Open the **Actions** tab.
2. Select **Build Zed Arabic Preview (Windows x64)**.
3. Press **Run workflow**.
4. When the run completes, open it and download the artifact named `zed-arabic-preview-x64`.

A push to `main` also starts a build.

## Important limitations

- This is an experimental source patch, not an official Zed release.
- The translation catalog is partial. Unknown strings remain in English.
- Arabic right alignment is applied to translated plain UI strings, but a full application-wide RTL layout pass is still needed.
- The workflow builds `zed.exe`; it does **not** create an official installer or bundle every optional companion component.
- The build may fail if upstream changes make the patch incompatible or if new build prerequisites are added.

## Upstream and licensing

Zed's source remains owned by Zed Industries and is used under the licenses in the upstream repository. This repository contains only the Arabic patch and the workflow used to build it. Review upstream licensing notices before redistributing a modified binary.

Upstream: https://github.com/zed-industries/zed
