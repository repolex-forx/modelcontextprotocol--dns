# Repolex Knowledge Graph of modelcontextprotocol/dns

RDF knowledge graph data for [modelcontextprotocol/dns](https://github.com/modelcontextprotocol/dns), parsed by [repolex](https://repolex.ai).

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
rlex download modelcontextprotocol/dns
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 54349d8c472352d0f738603743dc1bccc8e6027b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 54349d8c472352d0f738603743dc1bccc8e6027b
│           └── chunk-001.nq.gz
├── blob
│   ├── 01dc7f56687527823a704afb126bb22683ee19ca.nq.gz
│   ├── 09e8d66a384a653223f62232bcfdcaaf76952943.nq.gz
│   ├── 19b6a0d554172c7a1a67be0a92b127c53027d26a.nq.gz
│   ├── 2d7e72a047f62d7f94eac34259cbaf38ba4f100f.nq.gz
│   ├── 5c4a36d00326052ba0c59ea1b00b772fa5bc094a.nq.gz
│   ├── 61dfb6e4200eced251550367de849f7b5fd1ada4.nq.gz
│   ├── 666b583d3c059fb9a77a5bc6c57798d785c3b3db.nq.gz
│   ├── 67f955e18d6eadb645ca7e0b7c7ab61640981823.nq.gz
│   ├── 78ca4b6f0f5fdb85656b61123a8e8e4d062a7127.nq.gz
│   ├── 8e8e1fedc77ee90bb099b703785661489bcf146c.nq.gz
│   ├── a95cb0538ce3c313951a42f4a80b55f39421205a.nq.gz
│   ├── aff71c8f506c56b3a5baf743ea3c4514f44b41ce.nq.gz
│   ├── b3819ae8d37e3e2c3f8b372d2e77d0941c7b7807.nq.gz
│   ├── b5ae3014ad4b16f3c1b0cc76f226592e2b886cab.nq.gz
│   ├── bd7975772159fe2fc4f5d9f54afc7f161ccc9e94.nq.gz
│   ├── d0ded95b26c5024dabf388f7fa3caec18f14f885.nq.gz
│   └── ea3a70c6e532e1968f138b444a834437a4c78873.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 54349d8c472352d0f738603743dc1bccc8e6027b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 25 files
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

[modelcontextprotocol/dns](https://github.com/modelcontextprotocol/dns)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
