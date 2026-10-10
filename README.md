# Repolex Knowledge Graph of python-poetry/poetry-plugin-shell

RDF knowledge graph data for [python-poetry/poetry-plugin-shell](https://github.com/python-poetry/poetry-plugin-shell), parsed by [repolex](https://repolex.ai).

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
rlex download python-poetry/poetry-plugin-shell
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2d4261b00bfbe1ed3445366708eab1061bc5045c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2d4261b00bfbe1ed3445366708eab1061bc5045c
│           └── chunk-001.nq.gz
├── blob
│   ├── 1842aecbaea2d7c1ccb91a7dfdbb3fbe66dcaa8b.nq.gz
│   ├── 234ac850dc4806b18d467e88d44d80c123aa2789.nq.gz
│   ├── 25d8ee623c4b7e8c7e44cdacdc5eed9854d54d05.nq.gz
│   ├── 28c3da1f26683d97a391195e53429b0b50bd6c85.nq.gz
│   ├── 2d8eab61aef4bd24ecd270ab44380be402c1c930.nq.gz
│   ├── 3db8d0cfa4456087065bbe788718990d9a2b1c29.nq.gz
│   ├── 5c00c6abd23d0638428279ca1f42acdf6368072e.nq.gz
│   ├── 614d2f12e6f000af1d17031b577a4e3076e60457.nq.gz
│   ├── 6d8e802540d3c5c5f818582549750424b751b5c0.nq.gz
│   ├── 72c6d7e49dda6aac47561d358b34cc9136e1921e.nq.gz
│   ├── 7f4d2bd104d74846cb5110acb7d87f046faf1954.nq.gz
│   ├── 8b05732413290b8717603189211066f01001751a.nq.gz
│   ├── 902b4e4e47b3f225ee623a9805f2c2bcad3f3228.nq.gz
│   ├── c554e55bd04071beb119b3bc76f36e9375aaeb2a.nq.gz
│   ├── d2f165ea1470b0dee4c12e9b11c1cd883aacee5b.nq.gz
│   ├── e401b4805415b18006c1f531e73d6481a04c6425.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f362ee281312872c6729c7cd81198dd148df0006.nq.gz
│   └── f573549d194286684933330f6b1a2ab44d306a86.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2d4261b00bfbe1ed3445366708eab1061bc5045c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[python-poetry/poetry-plugin-shell](https://github.com/python-poetry/poetry-plugin-shell)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
