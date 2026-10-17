# Homebrew tap for Secure MCP Gateway

Formulae for [Secure MCP Gateway](https://github.com/ethan03805/Secure-MCP-Gateway), a local reference monitor between AI agent harnesses and MCP servers.

```sh
brew install ethan03805/tap/smcp
smcpctl install          # Standalone profile: launchd agent (macOS) or systemd user unit (Linux)
```

`Formula/smcp.rb` is written by the release workflow of Secure MCP Gateway (GoReleaser) for every tagged release. Its URLs point at the GitHub Release archives for darwin and linux (amd64 and arm64) and its SHA-256 values are those of the release checksum file, which is signed with minisign (key in the project's `SECURITY.md`) and with Sigstore cosign.

Do not edit `Formula/smcp.rb` by hand; the next release overwrites it. Report problems in the [main repository](https://github.com/ethan03805/Secure-MCP-Gateway/issues).

The formula installs the binaries only. Homebrew does not create the Gateway's configuration, keys or service; run `smcpctl install` (or `smcpctl bootstrap --dir <dir>`) afterwards. Remove with `smcpctl uninstall` and then `brew uninstall smcp`.
