# Portfolio

Projects I've built in my own time.

## [homelab](https://github.com/cons-tan-tan/homelab)

My home Kubernetes cluster on Proxmox VE. Infrastructure, hosts, and Kubernetes apps are managed declaratively with Terraform, Nix, and Flux, so I can rebuild everything from this repository when something breaks. Only application data is backed up.

The Minecraft servers in the cluster are reachable from the internet through a Linode VPS. The cluster connects out to the VPS over WireGuard, so no ports are opened at home.

## [pico-doorbell-detector](https://github.com/cons-tan-tan/pico-doorbell-detector)

TinyGo firmware for a Raspberry Pi Pico WH that listens for the doorbell and sends a notification to my phone through ntfy on the homelab. I made it because I often miss the doorbell while wearing headphones. It detects the chime from the ratio of its two tones, so it works regardless of volume or distance.

## [import-github-app-key](https://github.com/cons-tan-tan/import-github-app-key)

A Rust CLI that imports a GitHub App private key into AWS KMS or Google Cloud KMS, so that JWTs are signed inside KMS. The local PEM file is deleted only after the import succeeds. I wrote it for use at work, since I couldn't find anything other than copy-paste shell scripts.

## [dotfiles](https://github.com/cons-tan-tan/dotfiles)

A Nix flake for my development environments on macOS, WSL, and Linux. A new machine can be set up with two commands, even before GPG keys or secrets are available. CI checks all three platforms.
