# Repolex Knowledge Graph of urllib3/urllib3-secure-extra

RDF knowledge graph data for [urllib3/urllib3-secure-extra](https://github.com/urllib3/urllib3-secure-extra), parsed by [repolex](https://repolex.ai).

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
rlex download urllib3/urllib3-secure-extra
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b69da6320d82f1a08ff5035fb6bab917172b541e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b69da6320d82f1a08ff5035fb6bab917172b541e
│           └── chunk-001.nq.gz
├── blob
│   ├── 1a2397f1c2b6ecbce75b5c7829a02fab58cba289.nq.gz
│   ├── 221065e3bea106894d165337cc323fd097f8e59e.nq.gz
│   ├── 67db8902a00b72503d39cc8975a4028dcea5abc2.nq.gz
│   ├── 8acd8193a4bfbd3cc97d8696fe9cb539fd950275.nq.gz
│   ├── b1cb1601da8c7ca6231d4eebfe7debe6fe703c51.nq.gz
│   └── c0f207eedce6c22722e85ad15ceee53b9ca9b7da.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b69da6320d82f1a08ff5035fb6bab917172b541e.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 12 files
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

[urllib3/urllib3-secure-extra](https://github.com/urllib3/urllib3-secure-extra)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
