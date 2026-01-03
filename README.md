# Hindsight

**Hindsight** is a GitHub-style git activity visualizer for your terminal. It scans your local directories for git repositories and aggregates your contribution history into a beautiful, blue, pixel-perfect heatmap.

<img width="1140" height="705" alt="image" src="https://github.com/user-attachments/assets/629770d3-e876-48dd-8982-033b99112480" />


## Installation

```bash
cargo install hindsight
```

> You can get `cargo` [here](https://doc.rust-lang.org/cargo/getting-started/installation.html).

## Usage

```
hindsight [OPTIONS] [PATH]
```

### Interactive TUI (Default)

Run without arguments to scan the current directory and open the TUI:

```bash
hindsight
```

### Arguments

- `[PATH]`:  directory to scan (default: current dir)

### Options

| Flag | Description |
|------|-------------|
| `--days <N>` | Number of days to look back (default: 365) |
| `--depth <N>` | Max recursion depth for finding repos (default: 3) |
| `--authors "<NAMES>"` | Filter by comma-separated author list |
| `--list` | Print detailed stats table to stdout |
| `--export-tsv <FILE>` | Export stats to TSV file |

### Examples

**Analyze a specific workspace for the last 30 days:**
```bash
hindsight --days 30 ~/Dev
```

**Filter for your own commits:**
```bash
hindsight --authors "Alice,Alice Smith"
```

**Export your yearly stats to a file:**
```bash
hindsight --export-tsv 2024_stats.tsv
```

## License

MIT
