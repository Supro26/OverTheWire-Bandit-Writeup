# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a documentation repository containing writeups for the [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) wargame - a security challenge series teaching Linux command-line fundamentals. The repository is NOT a code project; it's markdown documentation.

## Repository Structure

- `levels/levelXX.md` - Individual level solutions (currently through level 18+, 23/34 completed)
- `ss/` - Terminal screenshots for visual reference
- `README.md` - Main documentation with progress tracking

## Key Information from README

- Bandit teaches: Linux fundamentals, file permissions, SSH, encoding/decoding, archive extraction, basic scripting
- 34 total levels, currently at level 24
- Each level file contains: Objective, Concepts Used, Commands Used, Explanation

## Working with This Repository

This is a documentation-only repository. There are no:
- Build commands
- Test commands
- Linting commands
- Development scripts

Common operations are standard git operations (add, commit, push) for adding new level solutions.

When adding new levels:
1. Create `levels/levelN.md` following the existing format
2. Add any relevant screenshots to `ss/`
3. Update progress count in README.md
