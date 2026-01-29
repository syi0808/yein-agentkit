# README.md Structure Guide

Generate a README.md with the sections below, in this exact order. Each section is required unless marked (optional).

Every piece of content must be derived from the actual codebase analysis. Do not fabricate features, commands, or requirements.

---

<sections>

## Section 1: Title & Badges

Use the project's display name as an H1 heading. Always include a license badge linking to the LICENSE file. Only add other badges (CI, version, coverage) if the corresponding infrastructure actually exists in the repo.

<example>
# Screenize

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
</example>

## Section 2: Introduction

Write exactly two elements:
1. **First sentence**: What the project is and what problem it solves. One sentence, no jargon.
2. **Second paragraph**: Why someone would use this over alternatives. Keep it to 2-3 sentences.

If the project has a UI, include a screenshot or demo GIF only if one actually exists in the repo. Do not add placeholders.

<example>
Screenize is a macOS screen recording application that captures screen content with mouse tracking and produces polished recordings with auto-zoom effects and custom cursor rendering.

Unlike basic screen recorders, Screenize uses a two-pass processing model: first capture raw video with mouse data, then apply intelligent zoom, click effects, and background styling in a timeline-based editor.
</example>

## Section 3: Key Features

Bullet list of 4-8 features. Each bullet has a bold title followed by a dash and a brief explanation. Only list features that exist in the code.

<example>
## Features

- **Screen & Window Capture** — Record entire screens or individual windows via ScreenCaptureKit
- **Mouse Tracking** — Automatic cursor position and click logging alongside video
- **Auto-Zoom** — Intelligent zoom keyframes generated from mouse data and UI analysis
- **Timeline Editor** — Edit zoom, cursor, and click effect keyframes on a visual timeline
- **Click Effects** — Configurable ripple animations on mouse clicks
- **Custom Cursors** — Replace the system cursor with styled alternatives in exports
- **Background Styling** — Apply backgrounds and padding to exported recordings
</example>

## Section 4: Getting Started

Write this section for **end users**, not developers. Focus on how to download, install, and set up the project to use it. Developer build instructions belong in CONTRIBUTING.md.

Adapt the subsections to the project type:
- **Application** → Requirements, Download, Setup (permissions, configuration)
- **CLI tool** → Requirements, Install (brew/cargo install/npm install -g/pip install), Verify
- **Library** → Requirements, Install (package manager command), Import

For Requirements: list the minimum OS/runtime version from config files. Do not include build tools (Xcode, compilers) — those are for contributors.

For Download/Install: use the distribution channel the user specified (GitHub Releases, package registry, website, etc.). If the project is only available as source, provide clone + build commands as a fallback.

For Setup: describe any first-run configuration, permissions, or environment setup the end user needs.

<example_application>
## Getting Started

### Requirements

- macOS 13.0 or later

### Download

Download the latest version from [GitHub Releases](https://github.com/user/screenize/releases).

Open the `.dmg` file and drag Screenize into the Applications folder.

### Setup

On first launch, Screenize will request the following permissions:

1. **Screen Recording** — Required to capture your screen
2. **Microphone** — Required for audio recording
3. **Accessibility** — Required for UI element detection and smart zoom

Grant each permission when prompted, or enable them manually under **System Settings > Privacy & Security**.
</example_application>

<example_cli>
## Getting Started

### Requirements

- Node.js 18 or later

### Install

```bash
npm install -g mytool
```

### Verify

```bash
mytool --version
```
</example_cli>

<example_library>
## Getting Started

### Requirements

- Python 3.10 or later

### Install

```bash
pip install mylib
```
</example_library>

## Section 5: Usage

1-3 basic usage examples. Adapt the format to the project type:
- CLI tool → show command examples with expected output
- Library → show code snippets with import and function calls
- Application → describe the primary workflow in numbered steps

<example>
## Usage

1. Launch Screenize and grant screen recording and accessibility permissions when prompted
2. Select a screen or window to record, then click Record
3. When finished, click Stop — the recording opens in the timeline editor
4. Adjust auto-generated zoom keyframes or add click effects as needed
5. Click Export to render the final video with all effects applied
</example>

## Section 6: Contributing

One short paragraph linking to CONTRIBUTING.md. Do not duplicate the contributing guide content here.

<example>
## Contributing

Contributions are welcome. Please read the [Contributing Guide](CONTRIBUTING.md) before submitting a pull request.
</example>

## Section 7: License

State the license type and link to the LICENSE file. Adjust the license name if the user chose something other than Apache 2.0.

<example>
## License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.
</example>

## Section 8: Author

Use the author or organization name provided by the user. Include a GitHub profile link if available from git config or user input.

<example>
## Author

**Jane Doe** — [GitHub](https://github.com/janedoe)
</example>

</sections>
