# Nationwide Car Owners Data Processing

This project processes a large dataset of car owners in China, performing various data cleaning and transformation tasks. The main objectives include translating headers, removing unnecessary columns, combining address fields, and chunking the data into smaller, manageable files.

## Table of Contents

- [Introduction](#introduction)
- [Data Processing Steps](#data-processing-steps)
- [File Structure](#file-structure)
- [Usage](#usage)
- [Validation](#validation)
- [Chunking](#chunking)
- [Final Merging](#final-merging)
- [Requirements](#requirements)
- [License](#license)

## Introduction

The dataset contains comprehensive information about car owners in China, including personal details, vehicle information, and contact information. This project aims to clean and transform the data for further analysis or storage.

## Data Processing Steps

1. **Load the Original CSV File**: The dataset is loaded into a Pandas DataFrame.
2. **Translate Headers**: Chinese headers are translated into English using a predefined mapping.
3. **Combine Address Fields**: Address components (Address, City, Province, Postal_Code) are combined into a single `Full_Address` field.
4. **Remove Unnecessary Columns**: Specific columns, including duplicates and those not needed for analysis, are dropped.
5. **Remove Duplicates**: Duplicate rows are eliminated to ensure data integrity.

## File Structure

- `760k-Car-Owners-Nationwide-China-csv-2020.csv`: The original dataset.
- `nationwide_trans.csv`: The dataset with translated headers.
- `nationwide_pan1.csv`: The cleaned dataset with unnecessary columns removed.
- `new_cleaned_chunks/`: A directory containing chunked CSV files of the cleaned dataset.
- `nationwide_cleaned_final.csv`: The final merged dataset after chunking.

## Usage

To use this project, you need to have Python and the Pandas library installed. Follow the steps below:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/nationwide-car-owners-data-processing.git
    cd nationwide-car-owners-data-processing
    ```

2. Install the required dependencies:
    ```bash
    pip install pandas
    ```

3. Run the data processing script:
    ```python
    python data_processing.py
    ```

Make sure to adjust the paths in the script if necessary.

## Validation

The validation steps ensure the integrity of the data throughout the processing. Key validation checks include:

- Checking for any 'Unnamed' columns in the final DataFrame.
- Verifying that the `Full_Address` field exists and contains combined address information.
- Ensuring that there are no duplicate rows.
- Confirming the presence of expected columns in the final dataset.

## Chunking

The cleaned dataset is divided into smaller chunks for easier handling. Each chunk is saved in the `new_cleaned_chunks/` directory. The number of chunks can be adjusted in the script.

## Final Merging

After chunking, all individual chunk files are merged into a final CSV file named `nationwide_cleaned_final.csv`, which contains the complete, cleaned dataset.

## Requirements

- Python 3.x
- Pandas library

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
