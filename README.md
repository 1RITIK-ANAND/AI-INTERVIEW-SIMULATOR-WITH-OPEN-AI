# AI_INTERVIEW_SIMULATOR
A Streamlit-based web application designed to help candidates practice technical interviews for roles like Python Developer, Data Analyst, and Frontend Developer. Powered by OpenAI's GPT-3.5, it generates role-specific questions, evaluates answers (via text or speech), provides feedback, and saves results for progress tracking.

Features
Role-Based Questions: Practice interviews for Python Developer, Data Analyst, or Frontend Developer roles with tailored questions.
Flexible Answer Input: Answer questions by typing or speaking, with speech-to-text powered by Google Speech Recognition.
AI-Powered Feedback: Get detailed feedback and a 1-10 rating for each answer using OpenAI's GPT-3.5 model.
Progress Tracking: Answers, feedback, and ratings are saved in a CSV file for performance analysis.
User-Friendly Interface: Built with Streamlit for an interactive and intuitive experience.
Modular Code: Organized into separate files for UI, logic, utilities, and role definitions.

Tech Stack
Python: Core programming language.
Streamlit: For the web-based user interface.
OpenAI API: For generating questions and evaluating answers.
SpeechRecognition & PyAudio: For speech-to-text functionality.
Pandas: For saving and managing results in CSV format.
Python-dotenv: For secure environment variable management.
Regular Expressions (re): For extracting ratings from feedback.

Project Structure

├── app.py                   # Main Streamlit application
├── interview_logic.py       # Logic for question generation and answer evaluation
├── utils.py                 # Speech-to-text utility functions
├── roles.py                 # Role and topic definitions
├── requirements.txt         # Python dependencies
├── .env                     # Environment variables (API keys)
├── .gitignore               # Git ignore file
├── .gitattributes           # Git attributes file
├── interview_results.csv    # Stores interview results (generated during use)
└── README.md                # Project documentation

Installation
Clone the Repository:
git clone https://github.com/your-username/ai-interview-simulator.git
cd ai-interview-simulator
Set Up a Virtual Environment (recommended):
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate



Install Dependencies:
pip install -r requirements.txt

Set Up Environment Variables:

Create a .env file in the project root.
Add your OpenAI API key:
OPENAI_API_KEY=your-openai-api-key
Obtain an API key from OpenAI.
Run the Application:
streamlit run app.py
The app will open in your default browser (typically at http://localhost:8501).

Usage
Enter Your Name: Provide your name to start the interview.
Select a Role: Choose from Python Developer, Data Analyst, or Frontend Developer.
Choose Answer Mode: Select "Type" to type answers or "Speak" to use speech-to-text.
Answer Questions: Respond to the displayed question via the chosen mode.
Evaluate Answer: Submit your answer to receive AI-generated feedback and a rating.
Track Progress: Results are saved in interview_results.csv for review.
Next Question or Restart: Move to the next question or restart the interview.

Example
Role: Python Developer
Topic: OOP in Python
Question: "Can you explain inheritance in OOP in Python?"
Answer: (Typed or spoken)
Feedback: Detailed feedback with a 1-10 rating, saved to CSV.

Challenges & Solutions
Speech Recognition Accuracy: Handled errors like UnknownValueError with user-friendly messages.
Rating Extraction: Used regular expressions to reliably extract 1-10 ratings from GPT feedback.
Data Management: Leveraged pandas for efficient CSV storage and appending.

Future Improvements
Add text-to-speech to read questions aloud.
Support multiple languages for questions and answers.
Expand roles and topics (e.g., Backend Developer, DevOps).
Integrate a dashboard to visualize performance trends from interview_results.csv.

Contributing
Contributions are welcome! To contribute:
Fork the repository.
Create a new branch (git checkout -b feature-name).
Commit your changes (git commit -m "Add feature").
Push to the branch (git push origin feature-name).
Open a Pull Request.
