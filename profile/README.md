<div align="center"> 
  
# `✨ Jvavscratch`

**Compile JavaScript into Scratch projects.**

<img width="256" height="256" alt="jvavscratch" src="https://github.com/user-attachments/assets/cc117258-a2a6-451a-99d3-47c1ae1a254a" />
</div>

---

## About Jvavscratch

Jvavscratch is an open-source compiler that bridges JavaScript and Scratch. You write your project
as ordinary JavaScript source files, and Jvavscratch compiles it **ahead of time** into a Scratch 3.0
project (`.sb3`) — the same format Scratch and TurboWarp already open.

It is a compiler, not an interpreter. There is no JavaScript runtime inside the generated project:
each AST node in your source is mapped onto a Scratch block opcode at build time, and the result is
written out as a native `project.json`. That means you can keep using the tooling you already
have — files, modules, Git, your editor's debugger — while the thing you produce is a normal
Scratch project.

### Highlights

- **Ahead-of-time compilation** — your source becomes Scratch blocks at build time, with no runtime layer in between.
- **Familiar language** — variables, functions, classes, inheritance, control flow, `async`/`await`, and more. The exact subset is documented in the [language reference](https://jvavscratch.github.io/docs/reference/language-reference).
- **Native output** — builds produce an ordinary `.sb3`, costumes and sounds included, ready to open in Scratch or TurboWarp.
- **Extensible compiler** — packages extend the compiler itself: they can contribute globals, block libraries, or override how an entire Babel node type is generated.
- **Round-trip capable** — `jvavscratch decompile` turns an existing `.sb3` back into source you can keep editing.

## Getting started

### Prerequisites

- [Node.js](https://nodejs.org) 18 or newer and npm.

### Install

The packages are distributed through GitHub rather than a package registry, so install the CLI
straight from the repository:

```bash
npm install -g github:Jvavscratch/cli
```

This gives you the `jvavscratch` command. (npm resolves the `@jvavscratch/*` dependencies the same
way and builds each one on install.)

### Create a project

```bash
jvavscratch new my-first-project
cd my-first-project
```

### Build it

```bash
jvavscratch build
```

The compiled project lands in `target/my-first-project.sb3`. To build and immediately open it in
TurboWarp, use `jvavscratch run` (Windows by default; other platforms can pass `--bypass`).

### Common commands

| Command | What it does |
| --- | --- |
| `jvavscratch init` | Scaffold a project in the current directory |
| `jvavscratch new [name] [path]` | Scaffold a new project |
| `jvavscratch build [path]` | Compile to `target/<name>.sb3` (`-o` enables the alpha optimiser) |
| `jvavscratch run [path]` | Build, then open the result in TurboWarp |
| `jvavscratch decompile <sb3>` | Turn an `.sb3` back into a jvavscratch project |
| `jvavscratch lib [name] [path]` | Scaffold a compiler-extension package |
| `jvavscratch add` / `remove` / `update` / `search` / `publish` | Manage packages |

Run `jvavscratch --help` for the full list.

## Project structure

A jvavscratch project looks like this:

```
my-project/
  jvavscratch.toml   # name, description, version, compiler options, [dependencies]
  project.d.json     # which sprites exist
  src/               # your JavaScript source, one file per sprite
    Sprite1.js
  lib/               # installed packages (must exist, even when empty)
  assets/
    stage/           # stage.json, backdrops, backdrops.json
    Sprite1/         # sprite.json, costumes/, sound/
  target/            # build output
```

## Documentation

Full documentation lives at **[jvavscratch.github.io/docs](https://jvavscratch.github.io/docs/)**,
in English and Chinese:

- **Guide** — installation, first project, and a worked tutorial
- **Grammar** — how JavaScript constructs map onto Scratch blocks
- **API** — the built-in libraries available from your source
- **Modules** — what each package in the organisation does
- **Language reference** — the authoritative description of the dialect

## Repositories

| Repository | Contents |
| --- | --- |
| [cli](https://github.com/Jvavscratch/cli) | The `jvavscratch` command |
| [core](https://github.com/Jvavscratch/core) | Compilation environment, AST dispatch, syntax transforms |
| [generator](https://github.com/Jvavscratch/generator) | Code generators, one per AST node type |
| [decompiler](https://github.com/Jvavscratch/decompiler) | `.sb3` back to source |
| [types](https://github.com/Jvavscratch/types) | The Scratch data model |
| [utils](https://github.com/Jvavscratch/utils) | Packaging helpers and the package-authoring API |
| [docs](https://github.com/Jvavscratch/docs) | The documentation site |

## License

Jvavscratch is released under the [Mozilla Public License 2.0](LICENSE).

## Contact

- **GitHub**: [https://github.com/Jvavscratch](https://github.com/Jvavscratch)
- **Email**: 2913335827@qq.com

---

<div align="center">
  <p>Made with ❤️ by the Jvavscratch Team</p>
</div>
