# Pseudocode to Code Generator

A Streamlit-based application that converts pseudocode into executable C++ code using a transformer model.

## Features
- Accepts pseudocode input and generates corresponding C++ code.
- Utilizes a custom tokenizer for efficient tokenization and encoding.
- Implements a transformer-based model for sequence-to-sequence generation.
- Supports CUDA for faster model inference (if available).

## Installation

### Prerequisites
- Python 3.8 or higher
- PyTorch
- Streamlit

### Step 1: Clone the repository
```bash
git clone https://github.com/yourusername/pseudocode-to-code.git
cd pseudocode-to-code
```

### Step 2: Set up a virtual environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Step 3: Install dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Ensure necessary files are in place
Ensure the following files are present in your project directory:
- `tokenizer.json`: Contains the tokenizer mappings.
- `transformer_model.pth`: Pre-trained transformer model weights.

## Usage

### Run the application
```bash
streamlit run app.py
```

### Instructions
1. Enter your pseudocode in the provided text area.
2. Click the "Generate Code" button.
3. View the generated C++ code in the output section.

## Example
Input Pseudocode:
```plaintext
Initialize a variable x to 5
Loop from 1 to 10
    Print x multiplied by the loop counter
```

Generated C++ Code:
```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 5;
    for (int i = 1; i <= 10; ++i) {
        cout << x * i << endl;
    }
    return 0;
}
```

## Model Details
- Transformer-based model with the following architecture:
    - 4 encoder and decoder layers
    - 256-dimensional embeddings
    - 4 attention heads
    - 1024 feed-forward dimensions
- Custom tokenizer for efficient text processing

## Custom Tokenizer
The tokenizer maps words and special tokens to integer IDs. Special tokens include:
- `<sos>`: Start of sequence
- `<eos>`: End of sequence
- `<pad>`: Padding token

## License
This project is licensed under the MIT License. See `LICENSE` for more information.

## Acknowledgments
- Inspired by modern NLP advancements and transformer models.
- Built using PyTorch and Streamlit.

