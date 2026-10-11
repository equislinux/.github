<div align="center">

# X Linux

**Arch-based, snapshot-first Linux with a script-driven installer and its own package tooling.**

[Website](https://equislinux.github.io/web/) · [Documentation](https://equislinux.github.io/web/en/docs/) · [Download](https://equislinux.github.io/web/download/latest/) · [Wiki](https://github.com/equislinux/wiki)

<img src="https://equislinux.github.io/web/showcase/hero-desktop.jpg" alt="X Linux — Hyprland desktop running xfetch" width="100%">

</div>

---

## Why X

- **Bootable generations (btrfs).** Every package transaction is captured as a
  snapshot with its own boot entry; roll back, diff, verify, pin and
  export/import (signed or encrypted) from the `x` CLI.
- **Multi-kernel, officially supported.** `linux`, `linux-lts` and `linux-zen`
  at install time and later (`x kernel install|remove`, with guard rails for the
  running and last kernel).
- **A real installer, in the terminal.** BIOS/UEFI, GRUB or systemd-boot, LUKS,
  dualboot, core or full (Hyprland) profile.
- **Signed repository and native tooling.** The `[x]` pacman repository is
  signed (`SigLevel = Required`); `xpm` (package manager) and `xpkg` (builder)
  drive a native `.xp` endpoint end-to-end.
- **WSL.** Importable rootfs plus a friendly first-run setup.

## Quick start

1. **Download** the latest ISO from
   [equislinux.github.io/web/download/latest](https://equislinux.github.io/web/download/latest/).
2. Flash it to a USB:
   `sudo dd if=x-<version>-x86_64.iso of=/dev/sdX bs=8M conv=fsync status=progress`
3. Boot it and follow the text installer. Full guide in
   [the docs](https://equislinux.github.io/web/en/docs/x/installer).

For Windows: the WSL rootfs is published in
[equislinux/wsl](https://github.com/equislinux/wsl) with provisioning in
[equislinux/wsl-scripts](https://github.com/equislinux/wsl-scripts).

## Repositories

| Repository | What it is |
|---|---|
| [`x`](https://github.com/equislinux/x) | The distro: archiso profile, text installer, ISO build |
| [`scripts`](https://github.com/equislinux/scripts) | Provisioning payload and `x` CLI (generations, setup, themes) |
| [`x-repo`](https://github.com/equislinux/x-repo) | Signed `[x]` package repository and portals |
| [`xpm`](https://github.com/equislinux/xpm) | Package manager (Rust, ALPM format, native `.xp`) |
| [`xpkg`](https://github.com/equislinux/xpkg) | Package builder (XBUILD/PKGBUILD to `.xp`) |
| [`wsl`](https://github.com/equislinux/wsl) | WSL rootfs and Windows importer |
| [`wsl-scripts`](https://github.com/equislinux/wsl-scripts) | WSL first-run setup |
| [`web`](https://github.com/equislinux/web) | Documentation portal (this site) |
| [`wiki`](https://github.com/equislinux/wiki) | Documentation sources (English/Spanish) |

## Contributing

Active development. Issues and PRs are welcome in any repository; for the
distro itself start with [`x`](https://github.com/equislinux/x). Documentation
exists in English and Spanish under [`wiki`](https://github.com/equislinux/wiki).

<sub>X Linux is an independent Arch-based spin, built with <code>mkarchiso</code>, btrfs, Rust and a lot of bash.</sub>
