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

## File Structure

Here's the updated **Project Structure** section, reflecting only the `app.py` and `app.html` setup:

---

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

---

Let me know if you'd like further refinements or additional details!

## How to Run

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install Anaconda (for managing dependencies and environments):

   - **macOS, Windows, Linux**:
     Follow the steps provided [here](#installing-anaconda-navigator).

3. Set up the environment:
   ```bash
   conda create --name sentiment-env python=3.12
   conda activate sentiment-env
   pip install -r requirements.txt
   ```

4. Start the server:
   ```bash
   python app.py
   ```

5. Open `app.html` in your web browser to interact with the application.

## Installing Anaconda Navigator

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

## Usage

1. Select your preferred language using the dropdown in the top-right corner.
2. Enter your text (one per line) in the provided input field.
3. Click "Analyze" to process the sentiment of the input text.
4. View the results on the "Result" tab.
5. To start a new analysis, click "New Analysis" and clear the input field.

## Customization

To add or modify supported languages, update the `translations` object in the `<script>` section of `app.html`.

## Example

Input:
```
I love programming.
This is terrible.
```

Output:
```
Text 1: I love programming.
Sentiment: Positive

Text 2: This is terrible.
Sentiment: Negative
```

## YouTube Demonstration

For a detailed walkthrough of the project, check out the demonstration video on [YouTube](#).

## Screenshots

Here are some screenshots of the application:

- **Input Tab:**
  ![Input Tab](screenshots/input-tab.png)

- **Result Tab:**
  ![Result Tab](screenshots/result-tab.png)

Add your screenshots in a `screenshots` directory and replace the paths above with the actual file paths.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any feature additions or bug fixes.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
