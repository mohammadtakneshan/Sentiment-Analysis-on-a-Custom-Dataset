# Natural-Language-Proj-2110

Features

	1.	User-Friendly Interface:
	•	Tabs allow seamless navigation between input and result sections.
	•	Placeholder and styling provide a clean, intuitive experience.
	2.	Multi-Line Input:
	•	The textarea supports large text inputs with scrolling and resizing.
	3.	Dynamic Result Display:
	•	Results are updated instantly without reloading the page.
	4.	Responsive Design:
	•	Compatible with various screen sizes and devices.

1. HTML Structure

The HTML document is divided into three main sections:
	•	Tabs Section: Allows switching between the Input and Result tabs.
	•	Input Tab: Includes a multi-line input field for users to type text and a submit button.
	•	Result Tab: Displays the sentiment analysis result.

2. CSS Styling

The CSS enhances the visual structure of the tabs, input area, and result display, ensuring the web page is user-friendly and responsive.

3. JavaScript Functionality

JavaScript handles:
	•	Tab switching logic.
	•	Sentiment analysis processing.
	•	Dynamically updating the result in the Result tab.

Code Components

1. Head Section

Contains metadata and styling information:
	•	Charset & Viewport Meta Tags: Ensures compatibility with different devices.
	•	CSS: Inline styles define the tab system, textarea styling, and overall layout.

2. Body Section

Tabs Section

<div class="tabs">
    <div class="tab active" data-tab="input-tab">Input</div>
    <div class="tab" data-tab="result-tab">Result</div>
</div>

	•	Tabs: Two clickable tabs (Input and Result).
	•	Active Class: Highlights the currently active tab.

Input Tab

<div id="input-tab" class="tab-content active">
    <div>
        <label for="text-input">
            Please enter a text in English:
        </label>
    </div>

    <div>
        <textarea id="text-input" name="text" maxlength="1000" placeholder="Type your text here..."></textarea>
    </div>

    <div>
        <button id="submit-btn" type="button">Submit</button>
    </div>
</div>

	•	Textarea:
	•	Allows multi-line input.
	•	maxlength: Limits input to 1000 characters.
	•	placeholder: Provides a hint to the user.
	•	Submit Button: Triggers the sentiment analysis logic.

Result Tab

<div id="result-tab" class="tab-content">
    <div>
        <strong>Result:</strong> 
        <span id="result-output">No analysis yet.</span>
    </div>
</div>

	•	Result Display: Updates dynamically with the analysis result.

3. CSS Styles

Enhances the visual layout:
	•	Tabs:

.tabs {
    display: flex;
    border-bottom: 2px solid #ccc;
    margin-bottom: 10px;
}
.tab {
    padding: 10px 20px;
    cursor: pointer;
    border: 1px solid #ccc;
    border-bottom: none;
    margin-right: 5px;
    background-color: #f9f9f9;
    border-radius: 5px 5px 0 0;
}

	•	Creates a clickable tab interface.
	•	Adds hover and active states for a user-friendly experience.

	•	Textarea:

textarea {
    width: 100%;
    height: 100px;
    resize: vertical; /* Allows resizing of the textarea vertically */
    overflow: auto; /* Ensures a scrollbar appears when needed */
}

	•	Makes the input field resizable.
	•	Adds scrollbars for better usability with large inputs.

4. JavaScript Functionality

Tab Switching Logic

const tabs = document.querySelectorAll('.tab');
const tabContents = document.querySelectorAll('.tab-content');

tabs.forEach(tab => {
    tab.addEventListener('click', () => {
        tabs.forEach(t => t.classList.remove('active'));
        tabContents.forEach(content => content.classList.remove('active'));
        tab.classList.add('active');
        document.getElementById(tab.dataset.tab).classList.add('active');
    });
});

	•	Enables users to toggle between the Input and Result tabs.
	•	Adds/removes the active class to display or hide corresponding content.

Sentiment Analysis Logic

document.getElementById('submit-btn').addEventListener('click', function() {
    const textInput = document.getElementById('text-input').value.trim();
    const resultOutput = document.getElementById('result-output');

    if (!textInput) {
        alert('Please enter some text.');
        return;
    }

    // Simulated sentiment analysis
    let sentiment = 'Neutral'; // Default sentiment
    if (textInput.includes('happy') || textInput.includes('great') || textInput.includes('good')) {
        sentiment = 'Positive';
    } else if (textInput.includes('sad') || textInput.includes('bad') || textInput.includes('angry')) {
        sentiment = 'Negative';
    }

    resultOutput.textContent = sentiment;

    // Switch to the Result tab
    tabs.forEach(t => t.classList.remove('active'));
    tabContents.forEach(content => content.classList.remove('active'));
    document.querySelector('[data-tab="result-tab"]').classList.add('active');
    document.getElementById('result-tab').classList.add('active');
});

	•	Logic:
	•	Fetches the user input from the textarea.
	•	Performs basic sentiment analysis (can be replaced with a more advanced algorithm).
	•	Dynamic Update:
	•	Displays the sentiment result in the Result tab.
	•	Automatically switches to the Result tab after analysis.

Usage Instructions

	1.	Open the web page in a browser.
	2.	Enter a text (max 1000 characters) in the Input tab’s textarea.
	3.	Click the Submit button to analyze the text.
	4.	View the sentiment result in the Result tab.



