# Vendor Sources

This repository vendors and adapts several upstream projects as plain files, not as Git submodules. Their original `.git` directories were moved into the root repository's internal `.git/vendor-repos/` backup area so this workspace can be pushed as one normal repository.

## Sources

| Directory | Upstream | Base commit |
| --- | --- | --- |
| `manuscript-writing/` | `https://github.com/YSLAB-ai/manuscript-writing.git` | `f83e99ff87c2dd4a76328e4f2d022685941c7246` |
| `slopbuster/` | `https://github.com/gabelul/slopbuster.git` | `38c68963da3d52ed6fd6ae4652763a69330e3fed` |
| `academic-writing-agents/` | `https://github.com/andrehuang/academic-writing-agents.git` | `d4d9d3a21afbccd4aee9237a70611429e7df4fba` |

## Local Purpose

The local changes adapt these tools for Polish academic writing, anti-GenAI-slop review, author-voice preservation, and thesis/paper workflows in Codex.
