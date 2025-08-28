# Examples

This directory contains example scripts and demonstrations for the AI vWS Sizing Advisor.

## Files

### `demo_model_extractor.py`
Interactive demo script for the ModelNameExtractor functionality. This script demonstrates how to:
- Extract model names from natural language queries
- Use enhanced keyword matching for model identification
- Test model matching with various input queries

#### Usage
```bash
cd examples
python demo_model_extractor.py
```

The script will start an interactive session where you can enter queries to test model name extraction.

#### Example Queries
- "I need llama 3 with 8 billion parameters"
- "Deploy mistral for chat"
- "What's the best 70B model?"

## Running Examples

Make sure you have the required dependencies installed:
```bash
pip install -r ../src/requirements.txt
```

Then navigate to this directory and run the desired example script.
