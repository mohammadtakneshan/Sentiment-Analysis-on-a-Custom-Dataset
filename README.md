# Sentiment Analysis on a Custom Dataset

## Overview

This project is a web-based application for performing **sentiment analysis** on a custom dataset. Users can input text, analyze sentiment, and view results interactively in multiple languages.

## Features

- **Multi-language Support**: Interface supports English, Spanish, Italian, French, and German.
- **Dynamic Tab Navigation**: Separate tabs for input and result views.
- **Responsive UI**: Mobile-friendly with an intuitive design.
- **Timeout Handling**: Requests timeout after 10 seconds to prevent long wait times.

## Technologies Used

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Python (to be provided in `app.py`)
- **Styling**: Custom CSS for a polished UI
- **API Endpoint**: `/analyze` for handling sentiment analysis

## Project Structure
```
├── app.py            
├── templates/
│   └── app.html        
├── LICENSE            
└── README.md          
```

### **Explanation**
- **`app.py`**:  
  This is the main Python backend application file. It handles:
  - Starting the Flask server.
  - Rendering the `app.html` file for the user interface.
  - Managing requests for sentiment analysis and processing user input.
  - Returning results to the frontend for display.

- **`templates/app.html`**:  
  This is the frontend HTML file that:
  - Provides the user interface for input and result visualization.
  - Contains the structure for language selection, text input, and sentiment analysis display.
  - Uses JavaScript for dynamic tab switching and event handling.

## Prerequisites
- **Python 3.12 or above**: This project is built and tested with Python 3.12. Using this version or newer is recommended for compatibility and optimal performance.
- **Anaconda**: For managing dependencies and environments easily.

### Installing Anaconda Navigator

1. **macOS**: 
   - Download the `.pkg` file from [Anaconda's official site](https://www.anaconda.com/products/distribution) and follow the installer instructions.
2. **Windows**: 
   - Download the `.exe` file and follow the installer.
3. **Linux**: 
   - Download the `.sh` file, then run:
     ```bash
     bash filename.sh
     ```

For detailed instructions, see the [official guide](https://www.anaconda.com/products/distribution).

### Why Use Anaconda?

Anaconda simplifies package management and environment setup, particularly for data science and machine learning projects. It helps:

- **Manage Dependencies**: Avoid conflicting versions of libraries.
- **Isolate Environments**: Each project can have its own Python version and dependencies.
- **Ease of Use**: Pre-installed libraries like NumPy, Pandas, and Jupyter simplify development.


---

## How to Run

### Steps

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install Anaconda** (for managing dependencies and environments):
   - macOS, Windows, Linux: Follow the steps provided in the [Installing Anaconda Navigator](#installing-anaconda-navigator) section below.

3. **Set up the environment**:
   ```bash
   conda create --name sentiment-env python=3.12
   conda activate sentiment-env
   pip install -r requirements.txt
   ```

4. **Start the server**:
   ```bash
   python app.py
   ```

5. **Open the application**:
   - Open the `templates/app.html` file in your web browser to interact with the application.

---

## How to Run

### Steps

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install Anaconda** (for managing dependencies and environments):
   - macOS, Windows, Linux: Follow the steps provided [here](#installing-anaconda-navigator).

3. **Set up the environment**:
   ```bash
   conda create --name sentiment-env python=3.12
   conda activate sentiment-env
   pip install -r requirements.txt
   ```

4. **Start the server**:
   ```bash
   python app.py
   ```

5. **Open the application**:
   - Open the `templates/app.html` file in your web browser to interact with the application.

---

## How to Use

1. Select your preferred language using the dropdown in the top-right corner.
2. Enter your text (one per line) in the provided input field.
3. Click "Analyze" to process the sentiment of the input text.
4. View the results on the "Result" tab.
5. To start a new analysis, click "New Analysis" and clear the input field.

## Customization

To add or modify supported languages, update the `translations` object in the `<script>` section of `app.html`.

## Sample Text

### English
I love it. 
This is great. 

It’s okay.
 It's not bad. 

I hate it. 
This is awful.

### French
J'adore.
C'est génial.

C'est pas mal.
Ce n'est pas mal.

Je déteste.
C'est horrible.


## YouTube Demonstration

For a detailed walkthrough of the project, check out the demonstration video on [YouTube](#).

## Screenshots

Here are some screenshots of the application:

- **Input Tab:**
  ![Input Tab](screenshots)

- **Result Tab:**
  ![Result Tab](screenshots)

Add your screenshots in a `screenshots` directory and replace the paths above with the actual file paths.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
