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

Three subsections: Prerequisites, Installation, Running.

For Prerequisites: list actual requirements found in config files (minimum OS version, runtime version, build tools). Do not guess — check `Package.swift`, `*.xcodeproj`, `Cargo.toml`, `package.json`, `pyproject.toml`, or equivalent.

For Installation: write the actual clone + build commands. Use the real build system.

For Running: explain how to launch or execute the project after building.

<example>
## Getting Started

### Prerequisites

- macOS 13.0 or later
- Xcode 15.0 or later

### Installation

```bash
git clone https://github.com/user/screenize.git
cd screenize
xcodebuild -project Screenize.xcodeproj -scheme Screenize -configuration Debug build
```

### Running

Open `Screenize.xcodeproj` in Xcode and press Cmd+R to build and run.
</example>

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
