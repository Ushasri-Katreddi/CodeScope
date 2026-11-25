# Build log

## 2026-11-24 · Phase 0 · Chapter 00 · Step 01

Inspected the empty workspace and created the approved documentation foundation. See the [bootstrap record](docs/03-implementation/00-project-bootstrap/01-workspace-preflight-and-bootstrap.md) for commands, files, errors and verification outcomes and the [handover](docs/09-session-logs/00-bootstrap-handover.md) for the next approval gate.

## 2026-11-24 · OpenCode research 01

Pinned OpenCode v2.4.1 and inspected release manifests and CLI dispatch. The [research record](docs/01-reverse-engineering/01-opencode-repository-and-entry-points.md) documents evidence and access failures. The next proposed step traces startup.


## 2026-11-25 · OpenCode 01 learning companion

Added 22 concept notes, two subsystem walkthroughs, two indexes and a session record. Updated the investigation with learning links, plus navigation, project state and learning tracker. Application tests were inapplicable. See the [learning session record](docs/09-session-logs/02-opencode-01-learning-handover.md).


## 2026-11-25 · OpenCode 01 concept visuals

Added one Mermaid diagram and a guided walkthrough to each of the 22 engineering concept notes. The [visual reading path](docs/04-engineering-concepts/README.md) connects package architecture, startup, dispatch, client-server messages and revision evidence.

PowerShell inserted the diagrams with WriteAllText and updated navigation with AppendAllText. A read-back check found exactly one fenced diagram and a walkthrough in each note, confirmed the evidence and revision headings remained present, and checked all ten added index destinations. Browser rendering was outside this check.

## 2026-11-25 · Phase 0 · Git setup

Initialized Git on main and configured the approved GitHub remote. The [publication step](docs/03-implementation/00-project-bootstrap/02-git-and-publication.md) records commands, observed output and verification.
