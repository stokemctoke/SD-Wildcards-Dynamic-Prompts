# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a wildcard/dynamic-prompt library for Stable Diffusion text-to-image generation. It provides lists of descriptive phrases that can be randomly selected to inject variation into image generation prompts. The library is organized by category (image types, character descriptions, environments, lighting, etc.).

## File Format and Structure

### CSV File Format
- **Location:** `csv/` directory
- **Naming convention:** `NN_Category-Name.csv` where:
  - `NN` is a zero-padded two-digit number (01, 02, 03, ...)
  - `Category-Name` is Title-Case-With-Hyphens
  
### Entry Format
Each CSV file contains one descriptive phrase per line:
- No header row
- No CSV structure (no commas, no quoting)
- Each line is a complete, evocative natural-language phrase (6–18 words typical)
- **Important:** Each line must end with **two trailing spaces** (this is the existing convention across all files and should be preserved)
- Phrases are written for image generation — descriptive and specific, not terse keywords

**Example entries:**
```
A rugged man with chiseled features and a stern expression
Neon-lit cyberpunk street scene with flying vehicles
Rim-lit silhouette against a blazing amber sunset
```

### Duplicates and Quality
- Check for duplicate lines within a file before committing: `sort <file> | uniq -d` should return empty
- The existing `02_Types-of-Men.csv` had a duplicate block (lines 29–56 were copies of 1–28); this was fixed

## Current File Structure

| File | Purpose | Entries |
|------|---------|---------|
| `01_Types-of-Image.csv` | Art styles, mediums, and rendering techniques | 84 |
| `02_Types-of-Men.csv` | Male character descriptions (facial features, demeanour, style) | 79 unique |
| `03_Types-of-Women.csv` | Female character descriptions | (stub, to be filled) |

## Adding New Entries or Files

1. **New entries in existing files:** Add one phrase per line, maintain formatting consistency (full phrases, two trailing spaces)
2. **New category files:** 
   - Create `csv/NN_Category-Name.csv` with the next number in sequence
   - Populate with 150+ entries for good randomisation variety
   - Follow the phrase format and trailing-space convention
   - No header row

## Key Points for Maintainers

- The two-trailing-space convention is intentional (carried from original files)
- Entries should be diverse and evocative — aimed at image generation quality, not brevity
- Line count matters: files with more entries provide better randomisation variation
- No comments, no structure — pure phrase lists
