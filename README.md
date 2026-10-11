# Repolex Knowledge Graph of jazzband/imaplib2

RDF knowledge graph data for [jazzband/imaplib2](https://github.com/jazzband/imaplib2), parsed by [repolex](https://repolex.ai).

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
rlex download jazzband/imaplib2
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6d45125882b80f71a68fcff1de9f6794c3c91815
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6d45125882b80f71a68fcff1de9f6794c3c91815
│           └── chunk-001.nq.gz
├── blob
│   ├── 002691475dde9759d32984937899f98cb47658c8.nq.gz
│   ├── 2cbc71bb30bb9f697184c37629292ae20291ae38.nq.gz
│   ├── 39eb8433c77ff0d544900d330978c3da2e9fd86f.nq.gz
│   ├── 4cec5e524200211b3ea4c6a875ab3b5d8021905f.nq.gz
│   ├── 506829703975f1887ec269945824df0d8df3d4cd.nq.gz
│   ├── 5b47b7b196c0bc9ea4c7b67cf88388b33b43a57c.nq.gz
│   ├── 5c0f4c246f3124527f7ca9f82b92cce8426c9947.nq.gz
│   ├── 6966869c7054c18810eb323772b93ba5a42cefc5.nq.gz
│   ├── 73846eb3696bf1bcfe9487e63e57684e4d0f80f1.nq.gz
│   ├── 7e949feddac606382f1b335cf56b0ab22086fef7.nq.gz
│   ├── 91ead4defda9e0d15ec7cd1c9d045762b6edce68.nq.gz
│   ├── 9243718034b1cabbfaa192071b60f719279d9300.nq.gz
│   ├── a65d04669c3dd34cfd1f4778e26734202f791bc2.nq.gz
│   ├── aa8741832fab599c886dfe0764a4ca6ea1d12657.nq.gz
│   ├── b0596f783a19143931227b49164d1e7f71b32d0a.nq.gz
│   ├── b369fdbd893933345752f8b3760b97c1697b309e.nq.gz
│   ├── b53fc50309eb05d04922778d6b257800770018b7.nq.gz
│   ├── beda28e821662c8d9fdefee034d83a5d75f9c023.nq.gz
│   ├── cba8be25b0baca7d11c44c64689d1b603bcd340c.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── e0d5efab56fb94577e7804603eb6f21f36977cb2.nq.gz
│   ├── e21712e4bd32da98507fe1f426b3a828488dcd07.nq.gz
│   ├── e37d37d1ff761edd35cc964a8da0bf4f986e93ad.nq.gz
│   ├── e613c337fdf417dd8fdd14014268187a14298b6e.nq.gz
│   ├── f8b2de2d6f838604196ef29098f4795e6430170b.nq.gz
│   └── fb0de3778e0f7cc64cabcd86a076a5dffcf5ac77.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6d45125882b80f71a68fcff1de9f6794c3c91815.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[jazzband/imaplib2](https://github.com/jazzband/imaplib2)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
