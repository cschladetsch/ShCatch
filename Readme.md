# BashCatch

A simple utility script for capturing command output in Bash.

## Description

BashCatch provides a `catch` command that captures both stdout and stderr output from shell commands, redirects the output to a specified file, and optionally copies the output to your clipboard.

## Features

- Captures both stdout and stderr in a single file
- Preserves the original command's exit code
- Option to automatically copy output to clipboard
- Simple syntax that works with any command

## Usage

```bash
catch [-c|--clipboard] output_file.txt command [args...]
```

### Options

- `-c` or `--clipboard`: Copy the captured output to clipboard

### Examples

Basic usage:
```bash
catch output.txt ls -la
```

Capture output and copy to clipboard:
```bash
catch -c results.txt grep "error" log.txt
```

## Installation

Clone this repository and add the script to your PATH, or create a symbolic link to it in a directory that's already in your PATH.

```bash
git clone https://github.com/yourusername/BashCatch.git
cd BashCatch
chmod +x catch
ln -s "$(pwd)/catch" ~/bin/catch  # Assuming ~/bin is in your PATH
```

## License

MIT