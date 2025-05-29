# PromptEngineeringRound2_CodeGeneration
Generate Python code from Google Docs instructions using various Transformer models like CodeT5 and DeepSeek Coder, and analyze prompt token counts.

# Code Generation and Prompt Analysis

This repository contains Python code to demonstrate generating code from natural language instructions using different Transformer models and analyzing the token counts of prompts. It utilizes the `transformers` library and integrates with Google Sheets for input data.

## Features

*   Code Generation: Use models like Salesforce/codet5p-220m and deepseek-ai/deepseek-coder-1.3b-instruct to generate Python code from text instructions.
*   Google Sheet Integration: Load instructions and team information directly from a Google Sheet (exported as CSV).
*   Prompt Engineering: Includes a manual pipeline setup for DeepSeek Coder to experiment with different prompt formats.
*   Token Counting: Analyze the token count of prompts using a specified tokenizer (e.g., gpt2).
*   Detailed Token Analysis: Break down token counts per prompt column and calculate the total per team.
*   CSV Export: Export token count results to a CSV file.

## Setup

1.  **Clone the repository**
2.  **Install dependencies**
3.  **Prepare your Google Sheet** Ensure your Google Sheet is structured with columns for Team Name and prompt instructions. Export it as a CSV file or use the public link.

## Usage

The code is designed to be run in a Jupyter Notebook or Google Colab environment. Each section in the provided code snippet can be run individually.

### Code Generation

Modify the `sheet_url` variable to point to your Google Sheet CSV export. Run the code cells that utilize the `transformers` library to load models and generate code based on the instructions in the sheet.

### Prompt Token Analysis

There are two methods for prompt token analysis:

1.  Using a direct Google Sheet URL:
    Modify the `sheet_url` variable and run the code cell that loads data directly from the URL and performs token counting.
2.  Uploading a CSV file:
    Run the code cells that use `google.colab.files.upload()` to upload your exported CSV file. The code will then load the data and perform token counting.

You can specify the prompt columns to analyze in the `prompt_cols` list or dictionary.

## Example

Refer to the provided code snippet for examples of how to load data, use the models for generation, and perform token counting.

## License

This project is licensed under the MIT License. 
