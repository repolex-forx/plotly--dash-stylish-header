# Repolex Knowledge Graph of plotly/dash-stylish-header

RDF knowledge graph data for [plotly/dash-stylish-header](https://github.com/plotly/dash-stylish-header), parsed by [repolex](https://repolex.ai).

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
rlex download plotly/dash-stylish-header
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 86f4faaa937852696983a0ed9cafc521e3bb022c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 86f4faaa937852696983a0ed9cafc521e3bb022c
│           └── chunk-001.nq.gz
├── blob
│   ├── 167025233296ea7fd508ab7e656d6add5de16fca.nq.gz
│   ├── 2af69c873479836963adcd5a36e9b36650ce827a.nq.gz
│   ├── 69b6ae1ca056f8e4954371966908d4a82dd32f72.nq.gz
│   ├── 6d101807b8ff4d7b8ef37e78356a5fc4825a483d.nq.gz
│   ├── 73ffaaabd5e4a84b6fb6d39933bff571d29b3706.nq.gz
│   └── 8ff2924ed2523b2c2d9e493117887d72181a110d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 86f4faaa937852696983a0ed9cafc521e3bb022c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 14 files
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

[plotly/dash-stylish-header](https://github.com/plotly/dash-stylish-header)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
