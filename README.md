# TOPSIS Python Package

## Overview

TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution) is a multi-criteria decision analysis (MCDA) method for ranking and selecting alternatives based on multiple criteria.

## Features

- Ranking of options based on multiple criteria
- Flexible weight and impact specification
- Ideal solution distance calculation
- CSV input and output support

## Installation

```bash
pip install topsis-package
```

## Usage

### Command-Line Syntax

```bash
python -m topsis.topsis <input_data.csv> <weights> <impacts> <result.csv>
```

### Parameters

1. `input_data.csv`: CSV file with options and criteria values
2. `<weights>`: Comma-separated criterion weights (e.g., "1,1,2,2,1")
3. `<impacts>`: Comma-separated criterion impacts ("+,+,-,-,-")
4. `result.csv`: Output CSV file for results

### Example

```bash
python -m topsis.topsis input_data.csv "1,1,2,2,1" "+,+,-,-,-" result.csv
```

## Input CSV Format

| Option   | Criterion1 | Criterion2 | Criterion3 | Criterion4 | Criterion5 |
|----------|------------|------------|------------|------------|------------|
| Option1  | 7          | 9          | 6          | 8          | 7          |
| Option2  | 8          | 7          | 9          | 7          | 8          |
| Option3  | 6          | 5          | 8          | 6          | 5          |

## Output CSV Format

| Option   | Distance from Ideal Best | Distance from Ideal Worst | TOPSIS Score | Rank |
|----------|--------------------------|----------------------------|--------------|------|
| Option1  | 2.5                      | 5.0                        | 0.6667       | 1    |
| Option2  | 3.0                      | 4.5                        | 0.6          | 2    |
| Option3  | 3.5                      | 3.0                        | 0.4615       | 3    |

## Requirements

- Python 3.6+
- Clean numerical input data

## License

© 2025 Shivane Kapoor
MIT License