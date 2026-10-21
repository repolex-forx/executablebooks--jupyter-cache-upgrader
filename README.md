# Repolex Knowledge Graph of executablebooks/jupyter-cache-upgrader

RDF knowledge graph data for [executablebooks/jupyter-cache-upgrader](https://github.com/executablebooks/jupyter-cache-upgrader), parsed by [repolex](https://repolex.ai).

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
rlex download executablebooks/jupyter-cache-upgrader
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3cb4c7c80b4d11e829289f833c4ff63b92a0c416
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3cb4c7c80b4d11e829289f833c4ff63b92a0c416
│           └── chunk-001.nq.gz
├── blob
│   ├── 017736cecb889c8af5e1eb9bf62a0cd1e2f47f85.nq.gz
│   ├── 36112a3c68590d6a8e07fea0ce70a5afb38c951a.nq.gz
│   ├── 98e4f9c44effe479ed38c66ba922e7bcc672916f.nq.gz
│   ├── b5bd98d32e203d1fc0a298ee24c7b3d3a20e1ad6.nq.gz
│   ├── cb9b46fd5c5821102a32d3c4eada9ee7b47b5737.nq.gz
│   ├── dd23a10898fc4dab9da3111d2216a8d86e959c7d.nq.gz
│   └── fbc4b07dcef98b20c6f96b642097f35e8433258e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3cb4c7c80b4d11e829289f833c4ff63b92a0c416.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 13 files
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

[executablebooks/jupyter-cache-upgrader](https://github.com/executablebooks/jupyter-cache-upgrader)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
