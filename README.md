# Quiz Maker

A tiny personal project I made to put the in-class quizzes that my professors hold on common quizzing sites like Wooclap, Kahoot, etc. into something I can actually use to test myself.

This app operates under the assumption that you have been given a set of questions and their accompanying answers, and it is simpler to use than some paid options on the market that drop features on you that you will never use. This is self-quizzing without all the bells and whistles.

## Features
### Quiz Builder
A simple form to create questions for your quiz.
- Question text box
- Option text box, with the ability to add multiple options as needed
- Correct answer check boxes
- Topic and explanation text boxes for tagging and correct answer explanations.
- Export to JSON

### Quiz Player
- Accept JSON quizzes from Quiz Builder
- Quiz-style answer selection (single answer radio buttons, multi-select check boxes)
- Wrong answer explanations

## Project Structure
```
.
├── static
│   ├── index.html
│   ├── quiz-builder.html
│   └── quiz-player.html
├── docker-compose.yml
├── Dockerfile
├── nginx.conf
└── README.md
```

## Prerequisites
- Docker

## Installation
1. Clone this repository
```bash
git clone https://github.com/rmmsia/quiz-maker.git
```

### Option A - Direct File Access
Just navigate to the project folder you cloned and open the files directly.

### Option B - Docker
If you prefer not to open your file explorer every single time you want to access the Quiz Builder and Player, you may use this option, though it may be **overkill for some users**.

2. Navigate to the project folder
```bash
cd quiz-maker
```

3. Build and start the container
```bash
docker compose up -d --build
```

4. Open in your browser at http://localhost:8080

### Option C - Without Docker
Another option for having an accessible URL without finding the static files in your file explorer, but without docker.

2. Navigate to the project folder
```bash
cd quiz-maker
```

3. Start a local server (Python3)
```bash
python3 -m http.server 8080
```

4. Open in your browser at http://localhost:8080