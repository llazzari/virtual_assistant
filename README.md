# Virtual Assistant

This Python-based virtual assistant takes voice input and executes one of the following tasks:
- **Search a keyword on YouTube**
- **Query information from Wikipedia**
- **Find the nearest drugstore**
- **Exit the program**

## Features
- Uses **SpeechRecognition** for voice input.
- Integrates with **YouTube search**, **Wikipedia API**, and **GeoPy** for location-based queries.
- Runs on **Windows** with a virtual environment for easy dependency management.

## Installation
### Prerequisites
Ensure you have **Python 3.7+** installed. If not, download it from [python.org](https://www.python.org/downloads/).

### 1️⃣ Create and Activate a Virtual Environment
```sh
python -m venv venv
```

- **Windows (Command Prompt)**:
  ```sh
  venv\Scripts\activate
  ```
- **Windows (PowerShell)**:
  ```sh
  venv\Scripts\Activate.ps1
  ```

### 2️⃣ Install Dependencies
```sh
pip install -r requirements.txt
```

## Usage
Run the virtual assistant:
```sh
python assistant.py
```

## Dependencies
Install the required libraries before running the script:
```sh
pip install SpeechRecognition wikipedia-api geopy requests
```

## How It Works
1. The assistant listens for voice input.
2. It processes the command and determines the action:
   - **"Search YouTube for [keyword]"** → Opens YouTube with the search results.
   - **"Search Wikipedia for [query]"** → Fetches a Wikipedia summary.
   - **"Find the nearest drugstore"** → Uses IP-based geolocation to find a nearby drugstore.
   - **"Exit"** → Terminates the program.
3. The result is displayed and, if applicable, a web browser opens with the relevant page.

## Troubleshooting
- If **microphone access fails in WSL**, run the script in **Windows** instead.
- If using PowerShell, ensure the execution policy allows script execution:
  ```sh
  Set-ExecutionPolicy Unrestricted -Scope Process
  ```
- If dependencies fail, try:
  ```sh
  pip install --upgrade pip
  pip install -r requirements.txt
  ```

## License
This project is licensed under the MIT License.

---

### 🚀 Future Enhancements
- Add more commands (e.g., weather updates, calendar integration).
- Improve voice recognition accuracy.
- Enable direct microphone access in WSL (via PulseAudio).

Feel free to contribute! 😊

