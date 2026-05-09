# SD-Wildcards-Dynamic-Prompts

A comprehensive library of dynamic prompt wildcards for **Stable Diffusion Automatic1111** and **Stable Diffusion Forge** users.

## Overview

This repository contains 20 CSV files with over 2,300 evocative, descriptive phrases organized by category. These wildcards enable random variation in your text-to-image prompts, allowing you to generate diverse, creative outputs without rewriting prompts manually.

## Supported Interfaces

- **Stable Diffusion Automatic1111** — Direct wildcard support via syntax: `{wildcard_category}`
- **Stable Diffusion Forge** — Full wildcard integration for dynamic prompt generation

## How It Works

In your prompt, reference any wildcard file by its category name:

```
A portrait of {03_Types-of-Women} wearing {11_Clothing-and-Fashion}, in a {04_Backgrounds-and-Settings}, with {05_Lighting-Conditions}
```

Each generation randomly selects one entry from the referenced CSV file, creating unique variations from a single prompt template.

## Library Categories

| # | Category | Entries | Purpose |
|---|----------|---------|---------|
| 01 | Types-of-Image | 84 | Art styles, mediums, rendering techniques |
| 02 | Types-of-Men | 79 | Male character descriptions |
| 03 | Types-of-Women | 166 | Female character descriptions |
| 04 | Backgrounds-and-Settings | 149 | Environments, locations, scenes |
| 05 | Lighting-Conditions | 128 | Light quality, mood, illumination |
| 06 | Colour-Palettes | 117 | Colour schemes, atmospheric mood |
| 07 | Shot-Types | 118 | Camera framing, lens language |
| 08 | Weather-and-Atmosphere | 120 | Environmental conditions, weather |
| 09 | Animals-and-Creatures | 126 | Fauna, fantasy creatures, wildlife |
| 10 | Objects-and-Props | 105 | Tools, furniture, vehicles, instruments |
| 11 | Clothing-and-Fashion | 112 | Garments, accessories, era styles |
| 12 | Hairstyles-and-Facial-Hair | 132 | Hair and beard variations, textures |
| 13 | Textures-and-Materials | 121 | Surface qualities, material finishes |
| 14 | Flowers-and-Plants | 113 | Flora, botanicals, garden elements |
| 15 | Mythological-and-Fantasy-Beings | 110 | Dragons, elves, demons, creatures |
| 16 | Occupations-and-Roles | 108 | Professions, character archetypes |
| 17 | Poses-and-Gestures | 121 | Body positions, actions, movement |
| 18 | Time-Periods-and-Eras | 110 | Historical periods, fashion eras, styles |
| 19 | Food-and-Drink | 109 | Culinary elements, dishes, beverages |
| 20 | Emotions-and-Expressions | 112 | Emotions, expressions, moods |

**Total: 2,340 entries**

## Installation

1. Clone or download this repository
2. Copy the `csv/` folder to your Stable Diffusion installation's `wildcards/` directory
3. Restart Stable Diffusion or reload wildcards

### Automatic1111 Path
```
stable-diffusion-webui/models/wildcards/
```

### Forge Path
```
stable-diffusion-forge/models/wildcards/
```

## Usage Example

### Simple variation:
```
A beautiful woman with a warm smile in a garden
{04_Backgrounds-and-Settings}
```

### Complex prompt with multiple wildcards:
```
A {02_Types-of-Men} with {12_Hairstyles-and-Facial-Hair}, {11_Clothing-and-Fashion}, 
standing in a {04_Backgrounds-and-Settings}, 
with {05_Lighting-Conditions}, 
{01_Types-of-Image}
```

Each generation will randomly select entries from the referenced files, creating unique variations.

## Phrase Format

Each entry is a complete, evocative natural-language phrase designed for image generation—not terse keywords. Examples:

- `A woman with delicate features and an ethereal presence`
- `A fog-drenched Victorian alley lit by gas lamps`
- `Rim-lit silhouette against a blazing amber sunset`
- `A mighty dragon guardian of treasure`

## Tips for Best Results

1. **Combine categories strategically** — Layer character + environment + lighting + mood for coherent scenes
2. **Use specific categories** — More specific wildcards yield better compositional control than generic ones
3. **Test and iterate** — Try different combinations to find what works best for your use case
4. **Balance randomness** — Mix fixed text with wildcards to maintain prompt intent while adding variation

## File Format

- Format: Plain text CSV (one phrase per line, no headers)
- Encoding: UTF-8
- Trailing spaces: Two spaces at end of each line (required for consistency)
- No commas, no quoting—pure phrase lists

## Contributing

To add entries or suggest improvements, submit a pull request or open an issue.

## License

Open for creative use. Feel free to adapt, extend, or redistribute for your Stable Diffusion workflow.
