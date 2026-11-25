# Engineering concepts for OpenCode 01

Start with the evidence and package layout, then follow the program from entry point to its architectural boundaries.

## Source evidence and package organization

1. [Git commits, branches, release tags and revision pinning](git-revision-pinning.md)
2. [MIT licensing](mit-licensing.md)
3. [Monorepo architecture](monorepo.md)
4. [Package manifests and package.json](package-json.md)
5. [Bun runtime and package management](bun.md)

## Language and tooling

6. [TypeScript](typescript.md)
7. [Effect](effect.md)
8. [OpenTUI](opentui.md)
9. [Solid](solid.md)
10. [Vite](vite.md)
11. [Turborepo](turborepo.md)
12. [Workspaces and workspace:* dependencies](workspaces.md)

## Startup and execution

13. [Application entry points](entry-points.md)
14. [CLI, TUI and GUI](cli-tui-gui.md)
15. [Command dispatch and command handlers](command-dispatch.md)
16. [Static imports and dynamic imports](imports.md)
17. [Lazy loading](lazy-loading.md)
18. [Language runtimes, command runtimes and agent runtimes](runtimes.md)

## Architectural boundaries and Git diagnostics

19. [Package boundaries and separation of concerns](package-boundaries.md)
20. [Client-server architecture](client-server.md)
21. [Protocols and schemas](protocols-schemas.md)
22. [The Git ls-remote command and observed proxy failure](git-ls-remote.md)

[Subsystem walkthroughs](../10-subsystem-learning-notes/README.md) · [Documentation home](../README.md)


## Visual reading path

1. Start with [Monorepo architecture](monorepo.md) and [Workspaces](workspaces.md) to see how packages are discovered and connected.
2. Follow [Application entry points](entry-points.md) into [Command dispatch](command-dispatch.md), then trace [Imports](imports.md) and [Lazy loading](lazy-loading.md).
3. Compare [Package boundaries](package-boundaries.md) with the [Client-server sequence](client-server.md). Package edges describe declared dependencies. Sequence arrows describe messages over time.
4. Read [Revision pinning](git-revision-pinning.md) alongside the [recorded proxy failure](git-ls-remote.md) to see how the evidence was recovered.

Each diagram is accompanied by guidance on which arrows or branches to follow. Captions identify verified OpenCode relationships, proposed CodeScope architecture, illustrative workflows, or observed command outcomes.
