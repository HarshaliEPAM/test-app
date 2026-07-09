# Quiz CLI

An interactive command-line quiz game for learning JavaScript and Node.js fundamentals.

The runnable application lives in the nested [`test-app/`](test-app/) directory. The repository root also contains a small `__MACOSX/` artifact directory, which is not part of the CLI application.

## Project Overview

This project is a Node.js command-line quiz game that lets you choose a category, pick how many questions to answer, and then play through an interactive quiz with progress tracking, answer explanations, and a replay option.

The app uses only built-in Node.js modules and local source files. No external npm dependencies are declared.

## Key Features

- Interactive terminal-based quiz experience
- Category selection at startup
- Question count selection per category
- Shuffled questions for each run
- Progress bar and question counter
- Immediate correct/incorrect feedback
- Explanations shown after each answer
- Final score summary with review of missed questions
- Replay support after completing a quiz
- ANSI color output for a clearer terminal UI

## Repository Structure

```text
.
├── README.md
├── __MACOSX/          # Unrelated artifact directory
└── test-app/          # Runnable Node.js CLI application
    ├── package.json
    ├── index.js       # Application entry point
    ├── data/
    │   └── questions.json
    └── src/
        ├── colors.js  # ANSI color/styling helpers
        ├── input.js   # readline-based input helpers
        └── quiz.js    # Quiz logic and results handling
```

## Prerequisites

- Node.js **18.0.0 or newer**
- npm (included with Node.js)

## Setup

From a fresh clone:

1. Open a terminal and go to the app directory:
   ```bash
   cd test-app
   ```
2. Install dependencies:
   ```bash
   npm install
   ```

   > This project does not currently declare any external dependencies, but running `npm install` is still the standard setup step and will prepare the local project environment.

## How to Run

Run the quiz from inside the `test-app/` directory:

```bash
npm start
```

You can also start it directly with Node.js:

```bash
node index.js
```

## How the Quiz Works

1. The app loads question data from `data/questions.json`.
2. It displays a welcome banner in the terminal.
3. You choose a category:
   - JavaScript Basics
   - Node.js Fundamentals
   - General Programming
4. You choose how many questions to answer.
5. The quiz runs question by question, showing:
   - available options
   - progress information
   - whether your answer is correct
   - the correct answer and explanation when needed
6. At the end, the app shows your score and a review of missed questions.
7. You can choose to play again.

## Test

Run the test command from the app directory:

```bash
npm test
```

There are currently no visible test files in the repository, so this command may not execute any tests yet.

## Technologies Used

- **Node.js** with ES modules
- **Built-in `fs/promises`** for loading quiz data
- **Built-in `readline`** for terminal input
- **ANSI escape codes** for terminal colors and styling
- **JSON** for quiz content storage

## Quiz Data

The bundled question set includes 15 total questions across 3 categories, with 5 questions in each category:

- JavaScript Basics
- Node.js Fundamentals
- General Programming

## Notes

- No build step is required.
- The entry point is `test-app/index.js`.
- The project is designed for an interactive terminal session, so it should be run in a local shell rather than a browser.

## Possible Future Improvements

- Add automated test coverage for the quiz logic and input helpers
- Expand the question bank with more categories and difficulty levels
- Add score history or persistence between runs
- Support random question selection from larger pools
- Add accessibility-focused terminal output options

## License

MIT
