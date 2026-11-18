<p align="center">
  <img src="https://raw.githubusercontent.com/bimeron/.github/main/profile/bimeron.png" alt="Bimeron logo" width="64" height="64">
</p>

<h1 align="center">Bimeron</h1>

<p align="center">
  Open-source VPN software: one networking core and native apps built on top of it.
</p>

Bimeron turns an access profile into a system VPN or a local SOCKS5 proxy.
[Bimeron Core](https://github.com/bimeron/bimeron-core) handles the network side: tunnel setup,
routing, DNS, reconnects and cleanup. The apps manage profiles and give each platform a native
interface.

## Projects

| Project | What it is | Platforms | Status |
| --- | --- | --- | --- |
| [Bimeron Core](https://github.com/bimeron/bimeron-core) | Go networking engine and CLI: system VPN or local SOCKS5 proxy, rule-based routing, IPC and embedding APIs | Windows, Linux, macOS; Android library (AAR) | [![Core release](https://img.shields.io/github/v/release/bimeron/bimeron-core?include_prereleases&label=pre-release)](https://github.com/bimeron/bimeron-core/releases) |
| [Bimeron Desktop](https://github.com/bimeron/bimeron-desktop) | Qt 6 app that manages profiles and connects in one click, without administrator rights | Windows, Linux | [![Desktop release](https://img.shields.io/github/v/release/bimeron/bimeron-desktop?include_prereleases&label=pre-release)](https://github.com/bimeron/bimeron-desktop/releases) |
| [Bimeron Android](https://github.com/bimeron/bimeron-android) | Kotlin and Jetpack Compose app with an embedded Core | Android | In development |
| [Bimeron Apple](https://github.com/bimeron/bimeron-apple) | Native SwiftUI apps | macOS, iPhone, iPad | In development |

All published builds are pre-releases. Packages are not code-signed yet, so compare each file's
SHA-256 with the value in its release notes before installing.

## How it fits together

- **Desktop:** Core runs as a system service and owns all privileged network operations. The
  Desktop app controls it over local IPC, so the interface itself runs without elevation. Each
  Desktop package includes a matching Core.
- **Mobile and Apple:** Core is embedded as a packet engine inside the platform VPN API
  (`VpnService` on Android, NetworkExtension on Apple platforms).
- **Profiles:** every component uses the same `.conf` profile format, so a profile created
  with the CLI works in the apps and the other way round.

Supported upstreams include Shadowsocks (including Shadowsocks 2022), VLESS, VMess, Trojan,
Hysteria2, TUIC v5, AnyTLS, NaiveProxy, MASQUE, SOCKS5, HTTP CONNECT and SSH. See the
[Core README](https://github.com/bimeron/bimeron-core#supported-upstreams) for transports and
limits.

## Get started

- **Use Bimeron on Windows or Linux:** download Bimeron Desktop from
  [Releases](https://github.com/bimeron/bimeron-desktop/releases).
- **Run a proxy or VPN from the command line:** follow
  [Try a local proxy](https://github.com/bimeron/bimeron-core#try-a-local-proxy).
- **Build your own app on the core:** start with
  [Integrate the core](https://github.com/bimeron/bimeron-core#integrate-the-core).

## Contributing and security

- Read the [contributing guide](https://github.com/bimeron/.github/blob/main/CONTRIBUTING.md)
  before opening a pull request.
- Report vulnerabilities privately as described in the
  [security policy](https://github.com/bimeron/.github/blob/main/SECURITY.md). Do not open
  public issues for them.
- For help, see [getting support](https://github.com/bimeron/.github/blob/main/SUPPORT.md).
