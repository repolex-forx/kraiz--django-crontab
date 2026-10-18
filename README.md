# Repolex Knowledge Graph of kraiz/django-crontab

RDF knowledge graph data for [kraiz/django-crontab](https://github.com/kraiz/django-crontab), parsed by [repolex](https://repolex.ai).

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
rlex download kraiz/django-crontab
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 978a26d547f1004ee286d08e31625bfbcee28811
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 978a26d547f1004ee286d08e31625bfbcee28811
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c71732acfe15c854f98914a5dcf74acb498a0af.nq.gz
│   ├── 1e43219ff061d4b87a9236ffec4ddb442931f095.nq.gz
│   ├── 2a9acf13daa95e85642ea255d3e3bd1ef8252804.nq.gz
│   ├── 3c7ad935456ce5ff6f43a933039892e451fb7851.nq.gz
│   ├── 456b07819dd848fe5af10ac04d827f9ebe8b33ca.nq.gz
│   ├── 4a5d97226606b8a46c72a088dd05e1c409648415.nq.gz
│   ├── 4addf2412e09342d1f7d0d767912245a22ac8d37.nq.gz
│   ├── 507a748f88e03f5d0826e2acdefa69ccf0634bbb.nq.gz
│   ├── 75cdc673cf158a4e754448f17309d41e993ad2b4.nq.gz
│   ├── 856691430f9c4f77981494b3b41eb8b525460410.nq.gz
│   ├── 8c1b798ef73cad70f71697c4e0889ab09e85c80f.nq.gz
│   ├── 98beb81d9d2c67b6f3532117bdf0561c3a4c62a0.nq.gz
│   ├── a53b22ba5387f69539970ef6150593da32b91aeb.nq.gz
│   ├── af0db39fd3b65b75e62517cc6a962f6f5348b556.nq.gz
│   ├── befff2c46153fcf6a3d0b8ff454b8419fd29277b.nq.gz
│   ├── e3b989792d76db8fe702f9bb4b6707106c98dbf2.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ffbc34ef72612929762ab3f58afa2488e4c061c1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 978a26d547f1004ee286d08e31625bfbcee28811.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[kraiz/django-crontab](https://github.com/kraiz/django-crontab)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
