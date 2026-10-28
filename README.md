# Repolex Knowledge Graph of spatialaudio/python-pa-ringbuffer

RDF knowledge graph data for [spatialaudio/python-pa-ringbuffer](https://github.com/spatialaudio/python-pa-ringbuffer), parsed by [repolex](https://repolex.ai).

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
rlex download spatialaudio/python-pa-ringbuffer
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3f5cae7470951907ba17cd66af000ab5ec255744
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3f5cae7470951907ba17cd66af000ab5ec255744
│           └── chunk-001.nq.gz
├── blob
│   ├── 291579928afd81f0cb95d02168b06228c27e2fea.nq.gz
│   ├── 5ace4600a1f26e6892982f3e2f069ebfab108d87.nq.gz
│   ├── 68847bb570e45dccf141cfd53ae086ae00c36099.nq.gz
│   ├── 7d61281032c8bace0359a5faf05a67235d42790d.nq.gz
│   ├── 8c5c92bc071f7de2bb7db1d7b2fc8e8d76c861db.nq.gz
│   ├── 95d58aa45365cbbdd79de80e18dcd66238e6974e.nq.gz
│   ├── cc91032a8ad4e894882604cdf551f9b84a546c10.nq.gz
│   ├── e4a38b2b74ef40b4b6a83c5674ec60fa5dc5d7ef.nq.gz
│   ├── f6eb9387c81efa4dcf81218bebf00f56db15195e.nq.gz
│   ├── f88489437d2a1a7f5dd86c70a95989e8e44cf12e.nq.gz
│   └── fe7972dab140d76e16e66530d48217d275c02c8f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3f5cae7470951907ba17cd66af000ab5ec255744.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 19 files
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

[spatialaudio/python-pa-ringbuffer](https://github.com/spatialaudio/python-pa-ringbuffer)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
