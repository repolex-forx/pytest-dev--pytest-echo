# Repolex Knowledge Graph of pytest-dev/pytest-echo

RDF knowledge graph data for [pytest-dev/pytest-echo](https://github.com/pytest-dev/pytest-echo), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-echo
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2d4d8d5e292158e7df171575dbac436cfaebb188
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2d4d8d5e292158e7df171575dbac436cfaebb188
│           └── chunk-001.nq.gz
├── blob
│   ├── 02c544dd676107fe350b87a21971863679b51a06.nq.gz
│   ├── 1b4a6bc67e6b05d3870921837c4900e310520fc9.nq.gz
│   ├── 28a416df60d43b62dbfc12789eb1b2a2011d7934.nq.gz
│   ├── 3a460b74c751445755916c559bc2d6388ca0b06b.nq.gz
│   ├── 4cfe7d3733501760c1ffc0ebfbf7271f0463d65c.nq.gz
│   ├── 4dc90799112a85fe04e500c6ab21f6f88c0e31a0.nq.gz
│   ├── 5cb02e5c9cbcc20007f2bf87bde3188a48f7f191.nq.gz
│   ├── 652d77a2dcd5b256661b4e4a96be029bb789e587.nq.gz
│   ├── 75ca8455e116a297966ec6a70650a33f2a1c3f5e.nq.gz
│   ├── 7c0b22938bbfa98c9b74acbb70fcc964cabb6f6e.nq.gz
│   ├── 7d92ca689101e945fb1b33ed661bfd11aa312c00.nq.gz
│   ├── 7f28b34fa30dbf7cce31f6c39ffb9fb6031e1df1.nq.gz
│   ├── 884270e32c27cde825d80153c489229bc5359673.nq.gz
│   ├── 8c3758bee5f5a9f71a7ec014d598b98edbfed52d.nq.gz
│   ├── 8c80a50bfad5f2946dedcdffb79cf594a99cb4d3.nq.gz
│   ├── 951adae819b0b4ec895b984a64203464f0d41c87.nq.gz
│   ├── b40def33522f3d5876ca039bf748823d86d2a826.nq.gz
│   ├── c03dd42ffdef49d4975d1da5ddbc51192acd4d6b.nq.gz
│   ├── c19ff26f57a5e4f264d187e741560423ffb95151.nq.gz
│   ├── c8c51b2d6e885eeaaafe9d3fe97327bfdd3f5309.nq.gz
│   ├── cd9b8135e767f4b0b83937e7d288c5cc84337837.nq.gz
│   ├── d31e222653ec988e19babb9292637480e03bad38.nq.gz
│   ├── d4bace00709a230db816526d96b1945428a44118.nq.gz
│   ├── e687d597dfdf81f7056bd8ade3819936c6bfc5cb.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fd9d35f2e7d68aa969246eac2c1a809f9e9a95ef.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2d4d8d5e292158e7df171575dbac436cfaebb188.nq.gz
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

[pytest-dev/pytest-echo](https://github.com/pytest-dev/pytest-echo)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
