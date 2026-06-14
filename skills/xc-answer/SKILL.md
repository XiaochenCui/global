---
name: xc-answer
description: "Find (xc: ...) markers in a file and respond to each with an Obsidian callout"
---

## Usage

Accepts one argument: a file path.

1. Read the file at the given path
2. Find all `(xc: ...)` patterns using regex `/\(xc:\s*([^)]+)\)/g`
3. For each match, interpret the content inside as a question, command, or prompt
4. Respond to each one by printing an [Obsidian callout](https://help.obsidian.md/callouts) block

Use callout types appropriately based on the context (e.g. `[!question]`, `[!info]`, `[!abstract]`, `[!tip]`).

### Output format

```
> [!question] xc: <captured text>
> Your answer here...
```

Answer each `(xc: ...)` match in order. If the file path argument is not provided, ask the user for it.
