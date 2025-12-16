# Porsche VIN Decoder

A web-based tool for decoding Porsche Vehicle Identification Numbers (VINs) from 1948 to present. Instantly decode any Porsche VIN to reveal detailed information about the model, year, factory, engine type, and more.

**[Try it now](https://crypto69.github.io/porsche-vin-decoder/)**

## Screenshots

![Porsche VIN Decoder - Main Interface](images/Vin%20Decoder1.webp)

![Porsche VIN Decoder - VIN Breakdown](images/Vin%20Decoder2.webp)

## Features

- **Comprehensive VIN Support**: Decodes VINs from 1948 to present day
- **Multiple Formats**: Supports both European/Rest of World and USA/Canada VIN formats
- **Visual Breakdown**: Color-coded character-by-character analysis of each VIN position
- **Detailed Information**: Reveals model, year, factory location, engine type, body style, and serial number
- **Example VINs**: Includes sample VINs for testing different Porsche models
- **Responsive Design**: Works on desktop and mobile devices
- **No Server Required**: Runs entirely in the browser with no backend dependencies

## Supported VIN Formats

| Format | Years | Length | Description |
|--------|-------|--------|-------------|
| 1981+ Europe/ROW | 1981-present | 17 chars | Modern European VINs (ZZZ filler) |
| 1981+ USA/Canada | 1981-present | 17 chars | North American VINs with body/engine codes |
| 1980 Transitional | 1980 | 10 chars | Transitional format with 'A' year code |
| 1970-1979 | 1970-1979 | 10 chars | Classic format with model/variant codes |
| 914/4 | 1970-1976 | 10 chars | Specific format for 914/4 models |
| 1969 | 1969 | 9 chars | Late 60s format |
| 1968 | 1968 | 8 chars | 1968 specific format |
| 1948-1968 | 1948-1968 | 5-6 chars | Early chassis numbers (356, early 911/912) |

## Supported Models

- **911 Series**: G-Model, 964, 993, 996, 997, 991, 992
- **Turbo Models**: 930, 911 Turbo variants
- **Front-Engine**: 924, 924 Turbo, 928, 944, 944 Turbo, 968
- **Mid-Engine**: Boxster (986, 987, 981, 982), Cayman, 718
- **SUVs**: Cayenne (955, 957, 958, current), Macan
- **Gran Turismo**: Panamera (970, 971)
- **Supercars**: 959, Carrera GT, 918 Spyder
- **Electric**: Taycan
- **Classic**: 356, 914/6, 912

## How to Use

1. Enter a Porsche VIN in the input field
2. Click "Decode VIN" or press Enter
3. View the decoded information including:
   - Vehicle summary (model, year, factory)
   - Visual VIN breakdown with color-coded positions
   - Detailed meaning of each VIN character

Alternatively, click on any of the example VINs to see a demonstration.

## Local Development

Simply open `index.html` in any modern web browser. No build tools or server required.

## Data Source

VIN decoding data is sourced from [Stuttcars](https://www.stuttcars.com/porsche-data/porsche-vin-decoder/).

## License

This project is provided for educational and personal use.
