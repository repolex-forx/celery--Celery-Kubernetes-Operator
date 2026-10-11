# Repolex Knowledge Graph of celery/Celery-Kubernetes-Operator

RDF knowledge graph data for [celery/Celery-Kubernetes-Operator](https://github.com/celery/Celery-Kubernetes-Operator), parsed by [repolex](https://repolex.ai).

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
rlex download celery/Celery-Kubernetes-Operator
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 622cfa832484f70a8541f03bd89d27ea0bae1e91
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 622cfa832484f70a8541f03bd89d27ea0bae1e91
│           └── chunk-001.nq.gz
├── blob
│   ├── 0512ae72779d4d24b1348bff292dc88431189072.nq.gz
│   ├── 05436b327dda4362e94be6a1780a5f5949eb6186.nq.gz
│   ├── 1742fed6d3bd80c5427204de2bfcd91ebf6f24a5.nq.gz
│   ├── 2e9fb0461bae577798cab2ce62f2ae8e532d79b8.nq.gz
│   ├── 3102d4164d5aa1a777b67b82daa32d012534a616.nq.gz
│   ├── 35cd86317dde025e8500f8af8e147d7eaf1f5f50.nq.gz
│   ├── 3602eb2465b025bd4ea48dedf8bf4e2adca0bf4b.nq.gz
│   ├── 40250704e8b9b657eb31b3290f31c6919e0243d2.nq.gz
│   ├── 424b3645e73f0f0ab54053b30a671859407e1b26.nq.gz
│   ├── 4495c0e0198a608e50dd295ccd67fd280c443f74.nq.gz
│   ├── 476cf8d85a89c33e07695f196ab8e56d26667559.nq.gz
│   ├── 5a574fd1cff4e4d6d42e8f2966463f787e13292d.nq.gz
│   ├── 5d2f03b2e2953ea657e6ef6f3571fb9f3801366b.nq.gz
│   ├── 60b342ab392e310d47433d00e2b48d3a4f74030e.nq.gz
│   ├── 6a97205f842b79e0114e7934ce3fc00959f4d51d.nq.gz
│   ├── 741e2833943659f8ffd675a52cae6d4653918e6a.nq.gz
│   ├── 79f332b568ea1fd940fdbca15b27a4751fc57312.nq.gz
│   ├── 865824471d19809f37b091197e654b51557046ed.nq.gz
│   ├── 8b1d3fa228f2940b45e2a88e1b84fb7f75872672.nq.gz
│   ├── 95717bcbf508114441a591ae86b19faaf6f289e1.nq.gz
│   ├── a025cb20d4d289d13bb1d0f77a936e33dc5b5639.nq.gz
│   ├── b6e47617de110dea7ca47e087ff1347cc2646eda.nq.gz
│   ├── b81de0423ba350a866115f06133ad2a6c5f03d54.nq.gz
│   ├── b9d85c1d1c1cbf4a1bd705785e8958b6e273454b.nq.gz
│   ├── bd23e067d6ccea3bf8f48fb4addd0ab6456f3767.nq.gz
│   ├── be4b59af4331a43549749a4611906f3eec68e66a.nq.gz
│   ├── c4192631f25b34d77a7f159aa0da0e3ae99c4ef4.nq.gz
│   ├── c908ffd428611f188df71dce299d9507c7a80b8d.nq.gz
│   ├── da06608910c84ce2e883bc8db75b65ae11410db5.nq.gz
│   └── f2bcee44aac60d8347eb5e1f6abea8af90fba61e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 622cfa832484f70a8541f03bd89d27ea0bae1e91.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[celery/Celery-Kubernetes-Operator](https://github.com/celery/Celery-Kubernetes-Operator)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
