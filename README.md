# Master's Research Repository

This repository contains all LaTeX sources for my Master's work. It is organized into two main folders:

- **`thesis/`** — Contains the complete master's thesis.
- **`proposal/`** — Contains the initial research proposal.

Each folder has its own `Makefile` for compiling the corresponding `.tex` document with bibliography and glossaries.



## Makefile Commands

Each `Makefile` supports the following targets:

### Compile the document
```bash
make
```

### Clean additional Latex files

```bash
make clean
```

For clearing and removing last pdf version use the following command

```
make distclean
```