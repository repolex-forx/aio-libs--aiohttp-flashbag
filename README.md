# Repolex Knowledge Graph of aio-libs/aiohttp-flashbag

RDF knowledge graph data for [aio-libs/aiohttp-flashbag](https://github.com/aio-libs/aiohttp-flashbag), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aiohttp-flashbag
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 705b31cca6fca1958f924931903bd1982719e281
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 705b31cca6fca1958f924931903bd1982719e281
│           └── chunk-001.nq.gz
├── blob
│   ├── 1af13ed8aafd41e5af4b27347e1e990ec3962275.nq.gz
│   ├── 22f69148cd5522300ef52890e3c26dfe87b95601.nq.gz
│   ├── 76da7b0ccde76e325f5ba9c661ba1b4c3c25cc45.nq.gz
│   ├── 7d2529e4c4a071f3ba59e04d0d99411580827365.nq.gz
│   ├── cd15dc0a42ba6fe26eecfe35ba5bdb37744ab1f3.nq.gz
│   ├── e24206f7951ce600070c653a55f024bdf4d78a08.nq.gz
│   ├── e29f967f4fb7652422474b8ea9dcbcd3b6cdb8fc.nq.gz
│   ├── e2c9a18aa54b5429e8342bfcf8ab8d512be06994.nq.gz
│   ├── e5ee1abbd2c6355805f2990223fff1b178334c1d.nq.gz
│   ├── f0db52773f0df1fb485b386087b553cb4ff39e9e.nq.gz
│   ├── f2e0a8560f8626423fdcf77adab3b71f1a589017.nq.gz
│   ├── f9419eaf4ea8ce367ed758d93bd50b13b125ec36.nq.gz
│   └── f95702ef847bb792ec3646370b8dad932f17efa2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 705b31cca6fca1958f924931903bd1982719e281.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 20 files
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

[aio-libs/aiohttp-flashbag](https://github.com/aio-libs/aiohttp-flashbag)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
