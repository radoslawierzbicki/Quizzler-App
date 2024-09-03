# Quizzler-App

This repository contains a simple quiz application built using Python. The application fetches trivia questions from an external API and presents them to the user in a graphical interface. The user can answer "True" or "False" to each question, and the application keeps track of the score. The quiz ends when there are no more questions left.

## How It Works

1. **Data Fetching (`data.py`)**:
   - The application retrieves trivia questions from the [Open Trivia Database (OpenTDB)](https://opentdb.com/) API.
   - It sends a GET request to the API with specified parameters (e.g., number of questions, type of questions) and processes the JSON response.
   - The retrieved questions are stored in a list of dictionaries, each containing the question text, the correct answer, and additional metadata.

2. **Question Model (`question_model.py`)**:
   - The `Question` class is defined here, which models a single quiz question.
   - Each `Question` object holds the text of the question and the correct answer.

3. **Quiz Logic (`quiz_brain.py`)**:
   - The `QuizBrain` class handles the quiz logic, including tracking the current question, checking answers, and calculating the score.
   - It determines if there are more questions to display and provides the next question when requested.
   - The class also manages the score based on the correctness of the user's answers.

4. **User Interface (`ui.py`)**:
   - The `QuizInterface` class creates a graphical user interface (GUI) using Python's Tkinter library.
   - The interface displays the questions, shows the score, and includes buttons for answering "True" or "False".
   - The GUI updates based on the user's interaction, providing feedback on correct or incorrect answers.

5. **Main File**:
   - The main script initializes the `QuizBrain` and `QuizInterface` objects, setting up the quiz for the user.
   - The quiz runs until all questions are answered, at which point the final score is displayed.
  
   
## Requirements

- Python 3.x
- `requests` library for fetching data from the API


