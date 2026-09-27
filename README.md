# Repolex Knowledge Graph of asimov-protocol/asimov-timeline-widget

RDF knowledge graph data for [asimov-protocol/asimov-timeline-widget](https://github.com/asimov-protocol/asimov-timeline-widget), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-protocol/asimov-timeline-widget
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 167ca052eefa6f50d74bd1b386cc55a6345759c4
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 167ca052eefa6f50d74bd1b386cc55a6345759c4.nq.gz
│   └── repolex
│       └── 167ca052eefa6f50d74bd1b386cc55a6345759c4
│           └── chunk-001.nq.gz
├── blob
│   ├── 11f02fe2a0061d6e6e1f271b21da95423b448b32.nq.gz
│   ├── 1ffef600d959ec9e396d5a260bd3f5b927b2cef8.nq.gz
│   ├── 2bd5a0a98a36cc08ada88b804d3be047e6aa5b8a.nq.gz
│   ├── 358ca9ba93f089b0133f05933f133a446402eb17.nq.gz
│   ├── 3d44b3d05ec0aafea98a06dbedbb8cd03553d981.nq.gz
│   ├── 56dd37d1e7305fbdaa77d94d899305044ae4509d.nq.gz
│   ├── 8aaa04d1763b3466a87486e9102733c7270533f0.nq.gz
│   ├── 91cf96db689ee79b0d4fa8a5aa278bb1bab75043.nq.gz
│   ├── 93996176ce4d2013d14eb9ec73c26cdf54ac3667.nq.gz
│   ├── 9c3198dfbf99c13c46b691c5c5b756a6e1f3d4b3.nq.gz
│   ├── a547bf36d8d11a4f89c59c144f24795749086dd1.nq.gz
│   ├── aa17831fd29319544f1acf318ab77f547cae23d0.nq.gz
│   ├── b0a64a269866d88c4ff0ff4eb1d50e2cefd2f1ce.nq.gz
│   ├── bd205e44a75a010818d1e4b3cffc3945518f7a2d.nq.gz
│   ├── caf6a4b7e76352e07777fd320db186fb85485648.nq.gz
│   ├── db0becc8b033a4a78144f4a3bb852082fe91cd62.nq.gz
│   ├── e24481e3b383e6089271c1019003e055e47df8f0.nq.gz
│   ├── e7564f71227f44ac1edbb32b28a6e6240b8be3cd.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f8db6d5afea8ddfabf13a79a6da4e38d4644346a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 167ca052eefa6f50d74bd1b386cc55a6345759c4.nq.gz
├── filetree
│   └── 167ca052eefa6f50d74bd1b386cc55a6345759c4.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 29 files
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

[asimov-protocol/asimov-timeline-widget](https://github.com/asimov-protocol/asimov-timeline-widget)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
