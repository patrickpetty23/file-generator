# Random File Generator

A Python script that generates various types of files with random content for testing purposes. Perfect for testing file sorting agents, backup systems, or any application that needs to handle diverse file types.

## Features

- **23 different file types** across multiple categories
- **Configurable output** via `.env` file
- **Random content generation** - each file contains unique, randomly generated data
- **File size control** - specify maximum file size (up to 100MB)
- **Random filenames** - various naming conventions for realistic testing

## Supported File Types

| Category | File Extensions |
|----------|----------------|
| **Documents** | `.txt`, `.pdf`, `.docx`, `.rtf`, `.md` |
| **Data/Config** | `.csv`, `.json`, `.xml`, `.yaml`, `.ini`, `.log` |
| **Web** | `.html`, `.svg` |
| **Spreadsheets** | `.xlsx` |
| **Presentations** | `.pptx` |
| **Images** | `.png`, `.jpg`, `.gif`, `.bmp` |
| **Databases** | `.sqlite`, `.parquet` |
| **Audio** | `.wav` |
| **Archives** | `.zip` |

## Installation

1. Clone or download this repository

2. Install required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

Copy `.env.example` to `.env` (or modify the existing `.env` file):

```bash
cp .env.example .env
```

Edit `.env` to configure the generator:

```env
# Path where generated files will be saved (relative or absolute)
OUTPUT_PATH=./generated_files

# Number of random files to generate
NUM_FILES=10

# Maximum file size in megabytes (capped at 100MB)
MAX_FILE_SIZE_MB=1
```

### Configuration Options

- **OUTPUT_PATH**: Directory where files will be created. Will be created if it doesn't exist.
- **NUM_FILES**: Total number of random files to generate.
- **MAX_FILE_SIZE_MB**: Maximum size for each file in megabytes. Automatically capped at 100MB.

## Usage

Run the script:

```bash
python generate_files.py
```

Or with Python 3 explicitly:

```bash
python3 generate_files.py
```

### Example Output

```
Random File Generator
==================================================
Output directory: /path/to/generated_files
Number of files: 10
Max file size: 1 MB
Available file types: 23
==================================================

[1/10] Generated: xk8f2j9d.pdf (pdf, 145.3 KB)
[2/10] Generated: alpha_beta.png (png, 892.1 KB)
[3/10] Generated: delta-4521.xlsx (xlsx, 67.8 KB)
[4/10] Generated: config_20260130_042.json (json, 12.4 KB)
[5/10] Generated: 3a7f9e1c.docx (docx, 234.5 KB)
...

==================================================
Generation complete!
Total files generated: 10
File type distribution:
  docx: 1
  json: 2
  pdf: 2
  png: 3
  pptx: 1
  xlsx: 1
Total size: 2.1 MB
```

## What Gets Generated?

Each file type contains realistic random content:

- **Text files** - Random paragraphs of lorem ipsum-style text
- **Images** - Random shapes, colors, gradients, and patterns
- **PDFs** - Multiple pages with random text, shapes, and colors
- **Spreadsheets** - Multiple sheets with random data tables
- **Presentations** - Multiple slides with random shapes and text
- **Word documents** - Formatted text with headings, lists, and tables
- **Databases** - Multiple tables with random data
- **CSV files** - Random tabular data
- **JSON/XML/YAML** - Nested random data structures
- **Audio files** - Random tones and sounds
- **ZIP archives** - Contains multiple random files

## Use Cases

- Testing file sorting and organization tools
- Training file management systems
- Testing backup and sync applications
- Generating test data for file processing pipelines
- Stress testing storage systems
- Creating diverse datasets for machine learning

## Requirements

- Python 3.7+
- Dependencies listed in `requirements.txt`:
  - python-dotenv
  - Pillow (PIL)
  - reportlab
  - openpyxl
  - python-pptx
  - python-docx
  - pandas
  - pyarrow

## Notes

- File types are selected at random with equal probability
- Filenames are randomly generated using various patterns
- Content is completely random and not meant to be meaningful
- The script respects the 100MB file size cap for safety
- All files are standalone and don't require external resources

## License

Free to use for any purpose.

## Contributing

Feel free to add more file types or generation patterns!
