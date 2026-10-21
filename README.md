# Repolex Knowledge Graph of graphql-python/swapi-graphene

RDF knowledge graph data for [graphql-python/swapi-graphene](https://github.com/graphql-python/swapi-graphene), parsed by [repolex](https://repolex.ai).

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
rlex download graphql-python/swapi-graphene
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5d92929640c6280ffd8f4f56f6f2361b4246939b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5d92929640c6280ffd8f4f56f6f2361b4246939b
│           └── chunk-001.nq.gz
├── blob
│   ├── 15c9f325a070ba2df64a0858cd158f6d6cdefa09.nq.gz
│   ├── 1a0c3c4e1d501bea3fe4877c040f7e0ed63c4b33.nq.gz
│   ├── 1fefc870c88028792baf5bf70a9ee56bf14514d3.nq.gz
│   ├── 254f7839810af4a414f06fa86ab5697e204eee11.nq.gz
│   ├── 2fb3c23924c716526a0c9f325ad6ce3cd4f96173.nq.gz
│   ├── 30a0408ff57de28bdb850d94248d5af5442cb102.nq.gz
│   ├── 40556ad7ef06398d1cd22388e827ef6eacf6b060.nq.gz
│   ├── 53504a329e5c9e82c1361be1ad1c51a73855ddcd.nq.gz
│   ├── 5510c2add6adf5c19c8f002c5c4deb1b0767a374.nq.gz
│   ├── 561d9d5733d9ca950221c4a3081d8d74a08a7d54.nq.gz
│   ├── 59de70a0b2710fee3a92e1929f3b824c8ae60fad.nq.gz
│   ├── 5c3c22669b66b2a63569eefa4be21ae44983ce07.nq.gz
│   ├── 5e57d72816ce2550db63252dd9b05e32350c36fe.nq.gz
│   ├── 6111388fe5c366cc720431322667a79b22950405.nq.gz
│   ├── 6c1476648ce8487225a7927ee23eda0429522e01.nq.gz
│   ├── 7297fa29fe0cf859ea3c7fa3830701f67cc4fe25.nq.gz
│   ├── 8deff0d545f79b7222dd335b55a6065ca4487f27.nq.gz
│   ├── 8fe914a6612e021b622375f3ed3f92cf166c7e26.nq.gz
│   ├── 91ea44a218fbd2f408430959283f0419c921093e.nq.gz
│   ├── 9354d93325a325cdeb5801c3b3dcc00efe717c05.nq.gz
│   ├── 9b45aa9ad69cc79c65ca4d7c57584a008e5f2c62.nq.gz
│   ├── b231b55cfbf85cc32c1980a33ad9526b0564d3b9.nq.gz
│   ├── c42a06ed6d270f008db2486d4c9216519ba19914.nq.gz
│   ├── c6225f157a87b00f40dcd0c6e2018c702fb7b506.nq.gz
│   ├── cc8b541fffe539134ba82918f45f01eadffbfb7c.nq.gz
│   ├── d07cb0ec630ff9a90149c007afbaae1f1887074b.nq.gz
│   ├── d2bbab1228b36ffb246e6e2a7f941eb7c8408075.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ee91966e526c80989399d76cbf5bd28d3a1824d8.nq.gz
│   ├── f260c1359dc8d7af2ee76b8c1267547419e1c284.nq.gz
│   └── fbbdd0cb0bbb62c90eff1afb15c02396ffe5ca2d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5d92929640c6280ffd8f4f56f6f2361b4246939b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[graphql-python/swapi-graphene](https://github.com/graphql-python/swapi-graphene)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
