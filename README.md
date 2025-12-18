# StardustSandbox.Assets

Repository that centralizes the **Stardust Sandbox** project assets as a reusable submodule. It contains images, fonts, music, shader effects, the pipeline configuration file (`assets.mgcb`) and other resources required by the MonoGame Content Pipeline.

## About

This repository serves as a single, versioned container for all game resources (assets) of **Stardust Sandbox**. Its purpose is to keep multimedia and configuration files separate from the main source code, enabling:

* Reuse across projects;
* Dedicated versioning for assets;
* Simplified workflows with the MonoGame Content Pipeline.

The main pipeline configuration file is `assets.mgcb` — it declares paths, properties and options for each asset and is processed by the Content Pipeline to produce `.xnb` files used at runtime.

## Structure and contents

Top-level example tree:

```bash
/ (root)
├─ assets.mgcb
├─ effects/      # shaders (.fx)
├─ fonts/        # .spritefont + .ttf
├─ songs/        # .wav
└─ textures/     # .png
```

Folder descriptions:

* `assets.mgcb` — MonoGame Content Pipeline file that lists and configures all assets.
* `effects/` — HLSL shaders with `.fx` extension.
* `fonts/` — font files: `.spritefont` (XML metadata) and `.ttf` TrueType font files. Both must remain together so the pipeline can generate the font properly.
* `songs/` — audio files (music) organized logically into subfolders by volume; standard format: `.wav`.
* `textures/` — graphical assets in `.png`.

## Conventions and rules

### General

* File names: **lowercase**, use underscore (`_`) for word separation.
* Organize assets into directories that reflect their type and logical usage.
* Keep metadata and source files together (e.g., `.spritefont` and `.ttf`).

### Standard formats

* Images: `.png`
* Audio (music): `.wav`
* Shaders: `.fx` (HLSL)
* Fonts: `.spritefont` + `.ttf`

### Color palette

* The project base palette is **AAP-64** (with small permitted deviations). Follow the palette when creating new art assets.

## Technical notes

* For building shaders and assets on **Linux**, consult the MonoGame documentation regarding Getting Started and the MGCB Editor. Depending on your distribution, extra dependencies or configuration for shader compilers may be required.
* To edit or preview `assets.mgcb`, install the **MGCB Editor** (MonoGame Pipeline Tool). The GUI provides an easier workflow to manage, import and configure asset properties.

## Contact

For asset-specific questions, issues or contributions, use the main project repository: `https://github.com/Starciad/StardustSandbox` (issues / PRs).
