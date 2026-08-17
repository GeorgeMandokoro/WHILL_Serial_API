<p align="center">
  <img src="docs/images/whill_logo.svg" alt="WHILL" width="100">
</p>
<h1 align="center">
  WHILL Serial API
</h1>

<p align="center">
  The serial (RS232C) command and data interface of the <b>WHILL Model CR2</b>, provided by WHILL, Inc.
</p>

<p align="center">
  <a href="https://whill.github.io/WHILL_Serial_API/"><b>whill.github.io/WHILL_Serial_API</b></a>
</p>

---

## Contents

| | |
|---|---|
| [**Specification**](https://whill.github.io/WHILL_Serial_API/spec/) | Frame format, control commands, state data, timing and connector pinout. Markdown source: [`docs/spec/`](docs/spec/WHILL_Serial_API_Specification.md) |
| [**Tester**](https://whill.github.io/WHILL_Serial_API/tester/) | Send commands to a real WHILL and watch the returned state data live. |
| [**Emulator**](https://whill.github.io/WHILL_Serial_API/emulator/) | Emulates a WHILL device — parses host commands and serves Dataset0 / Dataset1, so you can develop without hardware. |

The tester and emulator run entirely in the browser via the Web Serial API. No installation, no driver, no account.

## Requirements

| | |
|---|---|
| **Browser** | Chrome or Edge (Web Serial API — Safari and Firefox are not supported) |
| **Applies to** | Model CR2, Wheeled Robot Base, Electrical System Kit |
| **Not covered** | Omni-Platform (4WD) |
| **Transport** | RS232C, 38400 bps, 8-N-2 |
| **Connector** | D-sub 9-pin |
| **Serial API version** | 1.1 |

> Wheeled Robot Base and Electrical System Kit share the software specification of Model CR2 — every "Model CR2" description applies to them.

## Offline use

Each tool is a **single self-contained HTML file** with no external dependency. Use the *Download* link on the [site](https://whill.github.io/WHILL_Serial_API/) to save it with a version-stamped filename (e.g. `WHILL_Serial_API_Tester_v1.01.html`), then open it from a local disk — it works on an isolated network with no internet access.

Your data never leaves your machine: the tools communicate only between the browser and the WHILL over the serial port.

## Repository layout

```
docs/                 GitHub Pages root (Settings → Pages → main / docs)
├── index.html        Landing page
├── images/           Shared assets (logo, favicon)
├── spec/             Specification — Markdown source + exported index.html
├── tester/index.html Tester      (single self-contained file)
└── emulator/index.html Emulator  (single self-contained file)
```

`docs/spec/index.html` is exported from `WHILL_Serial_API_Specification.md`. When updating the specification, edit the Markdown, re-export, and commit both.

## License

Released under the MIT License. See [LICENSE](LICENSE).
