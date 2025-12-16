# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Porsche VIN Decoder - a single-page HTML application that decodes Vehicle Identification Numbers (VINs) for Porsche vehicles from 1948 to present. It supports both European/ROW and USA/Canada VIN formats.

## Architecture

The entire application is contained in `index.html`:

- **CSS** (lines 10-575): Dark theme with Porsche-inspired gold accent color (`#d4a574`). Uses CSS custom properties for theming.
- **HTML** (lines 577-653): Input section, error display, results section with summary card and VIN breakdown table.
- **JavaScript** (lines 655-1428): VIN decoding logic and DOM manipulation.

### VIN Data Structure

The `VIN_DATA` object contains comprehensive lookup tables for:
- Model year codes (1981-2029)
- Factory codes (Stuttgart, Neckarsulm, Leipzig, etc.)
- Model codes for EUR/ROW and USA markets
- Body types, engine types, airbag codes (USA)
- Historical variant codes (1968-1980)

### VIN Format Detection

The `detectVINFormat()` function determines format by length and content:
- 17 chars: 1981+ (EUR if positions 4-6 are "ZZZ", otherwise USA)
- 10 chars: 1970-1979 or 1980 (if position 3 is "A")
- 9 chars: 1969
- 8 chars: 1968
- 5-6 chars: 1948-1968 (early chassis numbers)

### Decoding Functions

Each format has a dedicated decoder:
- `decodeEURVIN()` - 1981+ Europe/ROW (17-char)
- `decodeUSAVIN()` - 1981+ USA/Canada (17-char)
- `decode1970sVIN()` - 1970-1979 (10-char)
- `decode1980VIN()` - 1980 transitional format
- `decode914VIN()` - 914/4 specific format
- `decode1968VIN()`, `decode1969VIN()` - Late 60s formats
- `decodeEarlyVIN()` - Pre-1968 chassis numbers

## Development

Open `index.html` directly in a browser - no build tools or server required.

## Data Source

VIN decoding data is sourced from Stuttcars (https://www.stuttcars.com/porsche-data/porsche-vin-decoder/).
