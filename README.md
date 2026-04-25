# π Synapse Link

A [pi](https://pi.dev) extension that expands wikilinks in your prompts into second-brain context from Logseq.

<p align="center">
  <img src="./images/logo.png" style="width: 300px; max-width: 100%;" />
</p>

## Overview

When you type a prompt containing wikilinks like `[[Coding]]`, this extension:

1. Extracts all `[[wikilink]]` patterns from your prompts
2. Passes them to `nt about <wikilinks> --agent` to recursively resolve
3. Appends the expanded context to your prompt before the agent processes it

Your knowledge, skills, instructions, etc. are automatically injected into conversations.

## Features

- **Automatic wikilink expansion** - Type one or more `[[Topic]]` links into your prompt
- **Recursive resolution** - Resolves `prerequisites` tags recursively
- **Agent filtering** - Uses `--agent` flag to exclude TODOs and noise
- **Fail gracefully** - Shows ⚠️ warning if a link can't be resolved

## Getting Started

Ensure these prerequisites are configured and work as intended:

- [Logseq](https://github.com/logseq/logseq)
- [nt](https://github.com/mlanza/nt)

For `nt` to work Logseq must be open and the api enabled.

Now the extension:

```bash
pi install https://github.com/mlanza/pi-synapse-link
```

## Usage

Key wikilinks into your π prompts

```
The job is [[Coding]] a Sokoban game using [[Atomic]].
```

and they get expanded and enriched with your Logseq content.  This can be skills, instructions — anything at all.

Since this only happens with wikilinks, omit them to interact with π as usual.

## License

[MIT](./LICENSE.md)
