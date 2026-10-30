# setup-wb

Install an exact [WB CLI](https://github.com/sneat-dev/wb) release in GitHub Actions without Go. This action installs the CLI only; workflows choose which commands to run.

`version` is required and must be an exact release tag. `expected-sha256` optionally supplies an independently obtained digest for the selected platform archive. The release checksum file detects corruption but cannot authenticate a release if both archive and checksum are replaced. Outputs include the installed release tag and binary path.

The action supports Linux, macOS, and Windows on amd64 and arm64 where the requested release publishes those assets. WB v0.203.0 publishes Linux and macOS archives, but no Windows archive; unsupported combinations fail explicitly.
