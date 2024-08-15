# LangChain and OpenAI GPT Integration

This project demonstrates how to integrate LangChain with OpenAI's GPT model to generate code snippets and their corresponding unit tests. The project structure includes `main.py`, `Pipfile`, `Pipfile.lock`, a `.env` file (containing the OpenAI API key), and a `.gitignore` file to hide the `.env` file from being pushed to GitHub.

## Project Structure

```sh
.
├── main.py
├── Pipfile
├── Pipfile.lock
├── .env
└── .gitignore
```

### Files Description

- `main.py`: The main script that integrates LangChain with OpenAI GPT to generate code and unit tests based on user input.
- `Pipfile` and `Pipfile.lock`: These files are used to manage project dependencies.
- `.env`: This file contains the OpenAI API key and is hidden from version control using `.gitignore`.
- `.gitignore`: This file ensures that sensitive files like `.env` are not pushed to GitHub.

## Setup and Installation

### Prerequisites

- Python 3.11
- Pipenv (for managing dependencies)

### Installation Steps

1. **Clone the Repository**

   ```bash
   git clone git@github.com:catchnaren/pycode.git
   cd pycode

   ```

2. **Install Dependencies**

   ```bash
   pip install pipenv
   pipenv install
   ```

3. **Set Up the .env File**

   Create a .env file in the root directory of the project and add your OpenAI API key:

   ```sh
   OPENAI_API_KEY=your_openai_api_key_here
   ```

4. **Activate the Virtual Environment**

   ```bash
   pipenv shell
   ```

## Usage

Run the main.py script with optional arguments for the task and language:

```bash
python main.py --task "return a list of numbers" --language "python"
```

## Example Output

```bash
> > > > > > > > GENERATED CODE:
> > > > > > > > def generate_numbers():

    return [1, 2, 3, 4, 5]

> > > > > > > > GENERATED TEST:
> > > > > > > > import unittest

class TestGenerateNumbers(unittest.TestCase):
  def test_generate_numbers(self):
  self.assertEqual(generate_numbers(), [1, 2, 3, 4, 5])

if __name__ == '__main__':
unittest.main()
```

## License

This project is licensed under the MIT License.

## Acknowledgements

- LangChain
- OpenAI
