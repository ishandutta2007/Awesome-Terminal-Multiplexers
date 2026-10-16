# Awesome-Terminal-Multiplexers

# Top Terminal Multiplexers Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Persistent Sessions, Pane Management & Terminal Workspace Orchestration*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Terminal Multiplexers**. These tools let you run multiple shell sessions inside a single terminal window, detach from them without killing running processes, and reattach later from anywhere — essential for remote server work, long-running jobs, and keyboard-driven workflows.

**Examples** include Tmux, GNU Screen, Zellij, Byobu, Terminator, Tilix, WezTerm, MobaXterm, SecureCRT, and Termius (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, persistent sessions, and transparent workspace management — ideal for developers, sysadmins, and anyone who lives in the terminal.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[MobaXterm](https://mobaxterm.mobatek.net/)**  
  Windows-only all-in-one remote toolbox with embedded X11 server, tabbed SSH, SFTP browser, and RDP/VNC support [citation:8]. Free Home Edition for personal use; Professional Edition for commercial deployment with advanced features [citation:3][citation:8]. Not a true multiplexer — session persistence is handled via saved sessions, not detached processes.

- **[SecureCRT](https://www.vandyke.com/)**  
  Commercial terminal emulator for Windows, macOS, and Linux with SSH, Telnet, serial, and rlogin protocols. Advanced session management, scripting, and secure file transfer. Closed-source, paid licensing.

- **[Termius](https://termius.com/)**  
  Cross-platform SSH client with sync across devices, SFTP, port forwarding, and team collaboration features. Free tier available; paid plans for advanced features.

- **[Royal TS](https://www.royalapps.com/)**  
  Commercial connection management tool supporting SSH, RDP, VNC, and remote desktop protocols with credential management and team sharing.

## Open-Source GitHub Projects

- **[tmux](https://github.com/tmux/tmux)**  
  **The standard terminal multiplexer** — allows persistent multiple "tabs" in a single terminal window, making it useful for long-running compilations, interactive multitasking, and pair programming [citation:6]. Start a session with `tmux new -s s1`, detach with `Ctrl-b d`, and reattach later with `tmux a -t s1` [citation:6]. Extensive configuration via `.tmux.conf` and a rich scriptable command interface. BSD-licensed.

- **[GNU Screen](https://www.gnu.org/software/screen/)**  
  **The original terminal multiplexer** — included in almost every Linux distribution by default, making it the most universally available option [citation:11]. Simple to learn with intuitive `Ctrl-a` prefix shortcuts: `Ctrl-a c` for new window, `Ctrl-a n` for next, `Ctrl-a p` for previous, `Ctrl-a d` to detach [citation:11]. Legacy systems support it even when tmux is unavailable [citation:11]. GPL-licensed.

- **[Zellij](https://github.com/zellij-org/zellij)**  
  **The friendly, batteries-included multiplexer** — a terminal workspace designed around the philosophy that you shouldn't sacrifice simplicity for power [citation:2][citation:7]. Out-of-the-box experience with mnemonic shortcuts displayed in the status bar, so you don't need to memorize anything [citation:2]. Supports **floating panes, stacked panes, layouts, session resurrection, and WebAssembly plugins** [citation:2][citation:7]. Mouse support for resizing panes by dragging dividers [citation:12]. Built-in web server for browser access and session sharing [citation:2]. Rust-based, MIT-licensed.

- **[Byobu](https://github.com/dustinkirkland/byobu)**  
  **Enhanced profile and configuration wrapper** for Screen and tmux — provides a more user-friendly interface with status notifications, tab management, and simplified configuration. GPL-licensed.

- **[Terminator](https://github.com/gnome-terminator/terminator)**  
  **Terminal emulator with built-in split panes** — arrange multiple terminals in a grid within a single window. Supports tabs, layouts, and customization via plugins. Python/GTK-based. GPL-licensed.

- **[Tilix](https://github.com/gnunn1/tilix)**  
  **Tiling terminal emulator for GNOME** — supports horizontal and vertical splits, tabs, and drag-and-drop pane rearrangement. Uses VTE for terminal emulation. MPL-2.0 licensed.

- **[WezTerm](https://github.com/wez/wezterm)**  
  **GPU-accelerated cross-platform terminal emulator and multiplexer** — written in Rust, supports tabs, panes, and workspaces with a built-in multiplexer that doesn't require tmux [citation:9]. Features native image rendering, ligature support, and container integration. MIT-licensed.

- **[Magmux](https://github.com/MadAppGang/magmux)**  
  **Terminal multiplexer with headless mode for CI and agent workflows** — designed to be driven by external controllers via socket, not just humans [citation:5]. Runs with no terminal at all when stdin is not a tty, making it usable from benchmarks and automated harnesses [citation:5]. Features pane splitting, VT-100 emulation, mouse support, and 1000-line scrollback per pane [citation:5]. Go-based.

- **[BDH Terminal Engine](https://pypi.org/project/bdh-terminal-engine/)**  
  **Lightweight pure C multiplexer with built-in modal text editor** — inspired by tmux and GNU Screen, with zero GUI dependencies [citation:10][citation:20]. Supports up to 18 concurrent sessions on Linux desktop, 8 in Termux mobile mode [citation:10]. Features built-in token scanner for URLs, IPs, and file paths, plus ASCII-mode web browsing via `links` [citation:10]. GPL-licensed.

- **[cy](https://github.com/cfoust/cy)**  
  **Time-traveling terminal multiplexer** — experimental alternative to tmux focused on replaying and searching through terminal sessions [citation:15]. Configuration via Janet programming language, with built-in fuzzy finding and shell command history insertion [citation:15]. Go-based.

### Additional Strong Open-Source Options

- **abduco** — Session management tool that provides detach/reattach for any terminal application, with dvtm as companion window manager.
- **dvtm** — Dynamic virtual terminal manager, often paired with abduco.
- **tmuxinator** — Ruby gem for managing complex tmux sessions via YAML project configs.
- **tmuxp** — Python-based tmux session manager and loader with YAML/JSON configs.
- **iTerm2** — macOS terminal emulator with native split panes and tmux integration for persistence.
- **Kitty** — GPU-accelerated terminal with native splits, tabs, and built-in multiplexing features [citation:9].
- **Ptyxis** — Modern container-aware terminal from GNOME with podman/distrobox integration [citation:9].

**Frameworks for building custom systems**: Combine **tmux** for proven stability and scriptability, **Zellij** for beginner-friendly power with floating panes and layouts, **WezTerm** for GPU-accelerated native multiplexing without external tools, and **Magmux** for headless/agent-driven automation workflows to build a complete terminal workspace tailored to your workflow.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Terminal multiplexers differ significantly in learning curve, configuration complexity, and feature scope. **tmux and Screen are proven but require memorizing keybindings** — Zellij prioritizes discoverability with on-screen shortcuts [citation:2]. Session persistence depends on the server remaining running; detaching does not survive a reboot.
- Self-hosted open-source solutions require proper configuration backup strategies and understanding of prefix-key navigation.

---

**Made for developers, system administrators, and anyone who works in the terminal.**  
Let's make terminal multiplexing more open, accessible, and keyboard-friendly.
