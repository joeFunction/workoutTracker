# workoutTracker# Unit 17 Nosql Homework: Workout Tracker

For this assignment, you'll create a workout tracker. You have already been provided with the front end code in the `Develop` folder. This assignment will require you to create Mongo database with a Mongoose schema and handle routes with Express.

## User Story

* As a user, I want to be able to view create and track daily workouts. I want to be able to log multiple exercises in a workout on a given day. I should also be able to track the name, type, weight, sets, reps, and duration of exercise. If the exercise is a cardio exercise, I should be able to track my distance traveled.

## Business Context

A consumer will reach their fitness goals quicker when they track their workout progress.

## Acceptance Criteria

When the user loads the page, they should be given the option to create a new workout, or continue with their last workout.

The user should be able to:

  * Add exercises to a previous workout plan.

  * Add new exercises to a new workout plan.

  * View multiple the combined weight of multiple exercises on the `stats` page.

## Commit Early and Often

One of the most important skills to master as a web developer is version control. Building the habit of committing via Git is important for two reasons:

1. Your commit history is a signal to employers that you are actively working on projects and learning new skills

2. Your commit history allows you to revert your code base in the event that you need to return to a previous state

Follow these guidelines for committing:

* Make single purpose commits for related changes to ensure a clean, manageable history. If you are fixing two issues, make two commits

* Write descriptive, meaningful commit messages so that you and anyone else looking at your repository can easily understand its history

* Don't commit half done work, for the sake of your collaborators (and your future self!)

* Test your application before you commit to ensure functionality at every step in the development process

We would like you to have well over 200 commits by graduation, so commit early and often!

## Submission on BCS

You are required to submit the following:

* The URL to the deployed application

* The URL to the Github repository

###########################################################
# UofT SCS Full-Stack Web Development Boot Camp Project #4: Code Quiz

# [Interview Camp](https://saltamay.github.io/UofT_BootCamp_CodeQuiz/)

A timed quiz application with multiple choice questions on JavaScript fundamentals that stores high scores for users to gauge progress compared to peers

## Table of Contents

1. [About the Project](#about-the-project)
2. [API(s) Used](#apis(s)-used)
3. [Development Strategy](#development-strategy)
4. [Additional Features](#additional-features)
5. [Getting Started](#getting-started) 
6. [Built With](#built-with)
7. [Test](#test)
8. [Licence](#licence)

## About the Project

As I proceed in my career as a web developer, I will probably be asked to complete a coding assessment. These assessments are typically a combination of multiple-choice questions and interactive challenges. As a bootcamp student, I want to build a code quiz application with multiple-choice questions on JavaScript that stores high scores so I can gauge my progress compared my peers. 

Initial design of the app has the following deliverables:

 * The user arrives at the landing page and is presented with a call-to-action to "Start Quiz." Also navigation options to "View Highscores" and the "Time" value set at 0.
 
 * Clicking the "Start Quiz" button presents the user with a series of questions. The timer is initialized with a value and immediately begins countdown.
 
 * Score is calculated by time remaining. Answering quickly and correctly results in a higher score. Answering incorrectly results in a time penalty (for example, 15 seconds are subtracted from time remaining).
 
 * When time runs out and/or all questions are answered, the user is presented with their final score and asked to enter their initials. Their final score and initials are then stored in `localStorage`.
 
 * It is also responsive and designed with mobile first principle.
 
 ## Minimun Requirements
 
 * Functional, deployed application.

 * GitHub repository with README describing project.

 * The first view of the application displays a button that starts the quiz.

 * Clicking the start button displays a series of questions.

 * Once the quiz begins, a timer starts.

 * If a question is answered incorrectly, additional time is subtracted from the timer.

* The timer stops when all questions have been answered or the timer reaches 0.

* After the game ends, the user can save their initials and score to a highscores view using local storage.

################################## Demo######################

![Demo My Code Quiz App](src/public/assets/showcase/demo.gif?raw=true)

## Development Strategy

1. Setup the ui where users can start the quiz or see the scores
2. Setup 'questions.js' that store questions in an object collection
3. Setup app.js that has the following functionalities:
    1. init() function that initilizes the app; this funtion will contain to _initialize the game_, like resetting scores or loading the   questions.
    2. startApp() function that starts the app; this task handles starting the game ex. show start page, display navigation, loads the  score from localStorage or sets up localStorage, listen for user click event
    3. startBtn_onClick(event) that handles the click event ex. show the questions, start the counter
    4. gameLogic() that deals with the game logic by starting the timer, and listen for click events of all quiz question buttons.
    5. quizBtns_onClick(event) that handles what to do when you click on a question's "answer button", call a function that determines if question is answered correctly (or not).
    6. determineIfQuestionIsRightOrWrong(question) given a question, determines if the answer is right or wrong if question is correct, change the score and add some points, if question is incorrect, change the score and decrease points
    7. changeTheScore(value) function will increase -or- decrease the score.
    8. endGame() function will ask for initials, update the local storage and score table
    
## Additional Features

* Add ui features to alert the user of correct or incorrect answers. Be sure to include the appropriate license.

* Customize the application theme.

* Create multiple quizzes and an option for users to choose between them.

* Add the application to personal portfolio.