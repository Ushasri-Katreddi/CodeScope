# Step 01 · Workspace preflight and documentation bootstrap

2026-11-24 · Phase 0 · Chapter 00. PowerShell workspace was D:\CodeScope. The root was pre-existing and empty. Its creation method and creator are unverified. The user approved the documentation bootstrap. No Git branch or commit was available.

## Preflight evidence

- `Get-Location`, `Get-ChildItem -Force`, and `@(Get-ChildItem -Force).Count` confirmed the current path and zero entries. Force includes hidden entries. `Test-Path -LiteralPath` returned false for root and parent AGENTS.md and local .git.
- `git rev-parse --show-toplevel` and `git status --short --branch` returned a repository error. They check the repository root and concise branch state. `rg --files --hidden -g '!**/.git/**'` listed no files during preflight.
- `Get-Command` and version checks showed Python and py 3.12.3, uv 0.12.5, Git 2.54.0.windows.1, Node 24.12.0, npm 11.7.0, Ollama client 0.40.15 and Docker CLI 29.9.2. Podman was absent from PATH. Ollama could not reach a server and `docker info --format '{{.ServerVersion}}'` was stopped without a server result.
- Windows runtime properties showed build 10.0.26300, x64 and four visible logical processors. `Get-CimInstance` hardware queries returned access denied. Read-only registry fallbacks identified Intel i3-8130U and Intel UHD Graphics 620. Python's Windows GlobalMemoryStatusEx call reported 8494747648 total and 857759744 available physical bytes. GPU acceleration remains unverified.
- `Get-PSDrive D` gave no usable free-space value. `python -c "import shutil; print(shutil.disk_usage('.'))"` returned 232900362240 free bytes. The -c flag runs the supplied Python source.
- `Get-Content -Encoding UTF8 -LiteralPath <attachment>` displayed the specification after the default decoding attempt produced garbled punctuation. `Get-FileHash -Algorithm SHA256` fingerprinted the source. OpenCode public identity was checked. A later fetch of the intended CodeScope repository returned a cache miss.

## Approved Bootstrap

Rechecked the empty directory with `Get-Location`, `Get-ChildItem -Force`, and `Test-Path -LiteralPath .git`. Ran `New-Item -ItemType Directory -Path 'docs/03-implementation/00-project-bootstrap','docs/09-session-logs','docs/templates'` to create the approved hierarchy. Ran `Copy-Item -LiteralPath <attachment> -Destination 'PROJECT_MASTER_PROMPT.md'` to preserve the exact bytes. This command group exited 0.

The patch editor stalled. A no-profile PowerShell inventory found the specification copy as the only root file. The documentation was then written with PowerShell using explicit UTF-8 encoding. Each root file describes its role. The documentation index links all six templates and the chapter record. No application code, dependencies, runtime tests or Git setup apply to this step.

## Reproduction and verification approach

From an empty workspace, repeat the path checks, create the directories, copy the original attachment, and write the approved Markdown. Compare SHA-256 hashes, enumerate files, validate relative Markdown paths, and check local Git state. Record the results below.

[Chapter](README.md) · [Project state](../../../PROJECT_STATE.md) · [Learning tracker](../../../LEARNING_TRACKER.md)

## Verification results

Verified 19 Markdown files and 37 relative links across authored documents. Source and copy SHA-256 both matched 4935D57F4C3EEF9194951A5CA521754D6D9D35072DAA6FFE33ABE77C7F311D3E. Git reported no repository and exited 128, as expected.

PowerShell used Get-FileHash, Get-ChildItem -Recurse -Force -File, Test-Path -LiteralPath, and git rev-parse --show-toplevel. Inline Markdown link destinations were checked against the filesystem. The preserved specification was excluded from link validation because it is a verbatim source artifact.
