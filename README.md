# Repolex Knowledge Graph of asimov-modules/asimov-anthropic-module

RDF knowledge graph data for [asimov-modules/asimov-anthropic-module](https://github.com/asimov-modules/asimov-anthropic-module), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download asimov-modules/asimov-anthropic-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 35f89a44acedde5f3b26db1a79b31060e2771643
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 35f89a44acedde5f3b26db1a79b31060e2771643.nq.gz
│   └── repolex
│       └── 35f89a44acedde5f3b26db1a79b31060e2771643
│           └── chunk-001.nq.gz
├── blob
│   ├── 0074ac243e97f58407fc5578ba1618c45bf1d23e.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 3755afb7c346537bdd473abdb3026712a0ee9fe5.nq.gz
│   ├── 4cd7a5bbf96083070f69994975a67204a299fd2d.nq.gz
│   ├── 6e8bf73aa550d4c57f6f35830f1bcdc7a4a62f38.nq.gz
│   ├── 6f83656972dcf4cdabab996bd49dde3986bc10be.nq.gz
│   ├── 7b1f124ff2e192ba4c9e5f48f18520573bdbee88.nq.gz
│   ├── 929f8adea61f2dba3d353e52cfb070983de3e28b.nq.gz
│   ├── b1863136531d27f34dd1707ec7b623f997f4f5d0.nq.gz
│   ├── b4e2a20bb6069d33479542fc863e7e36810e0f01.nq.gz
│   ├── b7f3a74ca7603fb0a6e32c31de0a52de3ac5befd.nq.gz
│   ├── b8ff9d4a92dba74196806770b3910c48e68f2b94.nq.gz
│   ├── bb67c988519445888ae76a7c7c4041de9dee75cf.nq.gz
│   ├── cc6f535b40f4ebf04221043237ff3deaf67f9549.nq.gz
│   ├── e245432111b81b4d50040da3d6bfaea388261f7a.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 35f89a44acedde5f3b26db1a79b31060e2771643.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 24 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[asimov-modules/asimov-anthropic-module](https://github.com/asimov-modules/asimov-anthropic-module)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
