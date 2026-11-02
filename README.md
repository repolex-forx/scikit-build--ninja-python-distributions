# Repolex Knowledge Graph of scikit-build/ninja-python-distributions

RDF knowledge graph data for [scikit-build/ninja-python-distributions](https://github.com/scikit-build/ninja-python-distributions), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-build/ninja-python-distributions
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0288ae7cb3669d458a7d0742da8f251b8a01de4a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0288ae7cb3669d458a7d0742da8f251b8a01de4a
│           └── chunk-001.nq.gz
├── blob
│   ├── 00a7b00c94e08b86c765d47689b6523148c46eec.nq.gz
│   ├── 08cfb571d39190941ecc945d0b2c3a478c0e1ab7.nq.gz
│   ├── 0b28ac4d47f9aa57f4fca777efe89fb75a1b6f0d.nq.gz
│   ├── 23fae44fa89f4cf6f9b45e979b98f2b2ece4e49e.nq.gz
│   ├── 252a4b8337015af7d975e3813f2d90071caa58bf.nq.gz
│   ├── 37ec93a14fdcd0d6e525d97c0cfa6b314eaa98d8.nq.gz
│   ├── 5043f4e044227eb36c7c361eaff12596d0ae6988.nq.gz
│   ├── 6381083e623970771911cc69733f4b8fa67d7ed3.nq.gz
│   ├── 727a55b3e1e5ad8fe1dd9e54af655f020773d414.nq.gz
│   ├── 7485d6a806699cad0c76041660b2225ca8b2923c.nq.gz
│   ├── 7a24d58224e8ba9761037f780b69214cd9e1a7fc.nq.gz
│   ├── 87772abf7bee12bc06c887a199e791989b8ccdbc.nq.gz
│   ├── 893ad72ab20add201886d2a46adc6493e7c72e6a.nq.gz
│   ├── 8fb235d7045be0330d94bcb3abd2ac43badaa197.nq.gz
│   ├── 9fb0be6e42bacd6009eb3a871b00e980d0908524.nq.gz
│   ├── a497968f1d98fe52ef0ec85e76baa5fa43a36a15.nq.gz
│   ├── b1b06c180f71d5a97709335823145b230576f2c5.nq.gz
│   ├── d4b1d477092bf4c37fcfd4e243ecce99ebb7f4b6.nq.gz
│   ├── d7f47867e64dd2f6de295bd82a4cee1d2054372d.nq.gz
│   ├── e267a20d1aa0ff4a751710302f4d883c173470f3.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e8f35eb1ba2eb5aa249ce09dbbce72bc6e14efef.nq.gz
│   ├── ed4a131595fa73ec81718fb4fae8cfeac5a07bd1.nq.gz
│   ├── ede1d527ea2e94acb2322373b71880ec31c83a3d.nq.gz
│   ├── f4c8ae521c62620e63853b384bd627fd1cb4c04b.nq.gz
│   ├── fa0442ce28dcc2e9c3710319176d5329440d9950.nq.gz
│   └── fa8f3e326bbe6dfe9026512a6094b81de4313694.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0288ae7cb3669d458a7d0742da8f251b8a01de4a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[scikit-build/ninja-python-distributions](https://github.com/scikit-build/ninja-python-distributions)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
