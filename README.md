# Repolex Knowledge Graph of UKPLab/acl25-nlp-contributions

RDF knowledge graph data for [UKPLab/acl25-nlp-contributions](https://github.com/UKPLab/acl25-nlp-contributions), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/acl25-nlp-contributions
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 553cdccabe8c06ac995704682c546bcfa1e6418e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 553cdccabe8c06ac995704682c546bcfa1e6418e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0f2ddb441d8fee6908a2ecf250285ff536fa5b79.nq.gz
│   ├── 13189fcd9f6da5a398c6153f6c495065813587c5.nq.gz
│   ├── 14411fd93d699377c6e17280cabaf9a39d67dbdc.nq.gz
│   ├── 229edba242bb190698662cdce6bdacde9f0769fe.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 3dc429a6613bf85898a47643fe31d4439fe9d973.nq.gz
│   ├── 4ba47a9e7ed4e9b9329420dfecccdd167a3495e2.nq.gz
│   ├── 51052caf4f043bd88fbad3f3b30d68da5f8eedc8.nq.gz
│   ├── 51fce782de336b4b2489d2256a53ebdddf185e29.nq.gz
│   ├── 668f729a9e3027c2d4dc41e99e7ca593ee650a77.nq.gz
│   ├── 68eb69b23434984ce6053d307b6b6b7f709a7e7e.nq.gz
│   ├── 698e9f972a96948e15606d89ceda254e571d2692.nq.gz
│   ├── 70b6fe260d9cf84f4e7074765086638590b39e60.nq.gz
│   ├── 7899506dcbf64f4dca7a47f6860caebbb34afc37.nq.gz
│   ├── 7b7fbb676349eccb069176fe34d679b0d8c275da.nq.gz
│   ├── 80f9dedb22582266a9daa4b5a74a2b7ef60f99a4.nq.gz
│   ├── 8871abfdc9c3745a372d1b55952f4d24481e3ea0.nq.gz
│   ├── 8b14d41f730e3642c5986d15e956bb8af5134367.nq.gz
│   ├── 94a0ec8b1b1e4226fa0f4bd9e853902fff7f6769.nq.gz
│   ├── 98d250b8f0b2ca80ce0876b0735bd8efe8dac1ae.nq.gz
│   ├── 9b3703a912d40f58fb0fb57d20742e53d9fe7671.nq.gz
│   ├── 9ccec457225a28cf619811206e2f79fca41e7ede.nq.gz
│   ├── a1fe583ff41f5e00a9b0e6481da10f507d16d31f.nq.gz
│   ├── a70d291241eea483a3e2ca58d7c779b17cc164b8.nq.gz
│   ├── c08a79032592be8f5e7318991b0242323389469d.nq.gz
│   ├── c6718de5c5ae59d2c22141a147f5afba41af9cbb.nq.gz
│   ├── c7be7fec3487002c00de6168878d11fd2dabff7d.nq.gz
│   ├── d62fc66df4b9acdd5381753fde4173a5775b1ddf.nq.gz
│   ├── ed3a9d377ba3c30e6eb8b2a35e08e8dc814a0725.nq.gz
│   └── f47c06cc18baa434989aa2d46756a0b678957242.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 553cdccabe8c06ac995704682c546bcfa1e6418e.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 37 files
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

[UKPLab/acl25-nlp-contributions](https://github.com/UKPLab/acl25-nlp-contributions)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
