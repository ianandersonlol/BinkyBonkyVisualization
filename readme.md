# BinkyBonkyVisualization

This Python script, `BinkyBonkyVisualization.py`, automates the process of generating a Python plotting script using OpenAI's GPT-4 model. The generated script helps visualize the most biologically relevant data from a given CSV file. The figure produced by the script will have a relevant title that also credits BinkyBonky.

## Table of Contents

1. [Requirements](#requirements)
2. [Usage](#usage)
3. [Function Overview](#function-overview)

## Requirements

To use this script, you need the following Python packages installed:

- `sys`
- `pandas`
- `openai`

You also need an OpenAI API key, which you can obtain by signing up for an account on the [OpenAI website](https://beta.openai.com/signup/).

## Usage

To use this script, you need to provide the CSV file path as a command-line argument. The script will generate a Python plotting script based on the data in the file and save it with the format `<base_filename>_figuregen.py`.

```bash
python BinkyBonkyVisualization.py path/to/your/csvfile.csv
```

## Function Overview

### `generate_plotting_script(file_path)`

This function takes a file path to a CSV file as input. It reads the CSV file and extracts relevant information such as column names, the first two rows of data, and the number of rows. Then, it uses the OpenAI API to generate a Python plotting script based on this information. The generated script is saved as a new Python file with the format `<base_filename>_figuregen.py`.

- `file_path`: The file path to the CSV file containing the data to be visualized.

### `if __name__ == "__main__":`

This block of code is executed when the script is run directly. It checks if the correct number of arguments is provided and calls the `generate_plotting_script()` function with the provided file path.
