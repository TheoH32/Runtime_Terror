---
title: Binary Quiz
layout: page
description: "The final test of knowledge!"
image: assets/images/pic07.jpg
nav-menu: true
---


<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dog Matcher Quiz!</title>
</head>

<body>
    <div class="container">
        <div id="game" class="justify-center flex-column">
          <div id="hud">
            <div id="hud-item">
              <p class="hud-prefix">
              </p>
              <h1 class="hud-main-text" id="questionCounter">
              1/3
              </h1>
            </div>
          </div>
            <h2 id="question">What personality do you want your dog to have?</h2>
            <div class="choice-container">
                <small class="choice-prefix">A</small>
                <small class="choice-text" data-number="1">Choice 1</small>
            </div>
            <div class="choice-container">
                <small class="choice-prefix">B</small>
                <small class="choice-text" data-number="2">Choice 2</small>
            </div>
            <div class="choice-container">
                <small class="choice-prefix">C</small>
                <small class="choice-text" data-number="3">Choice 3</small>
            </div>
            <div class="choice-container">
                <small class="choice-prefix">D</small>
                <small class="choice-text" data-number="4">Choice 4</small>
            </div>
        </div>
    </div>
</body>



<style>

  .choice-container {
    display: flex;
    margin-bottom: 0.5rem;
    width: 100%;
    font-size: 1.8rem;
    border: 0.1rem solid rgb(86, 165, 235, 0.25);
    background-color: white;
  }

  .choice-container:hover {
    cursor: pointer;
    box-shadow: 0 0.4rem 1.4rem 0 rgba(86, 185, 235, 0.5);
    transform: translateY(-0.1rem);
    transition: transform 150ms;
  }

  .choice-prefix {
    padding: 1.5rem 2.5rem;
    background-color: #380df2;
    color: white;
  }

  .choice-text {
    padding: 1.5rem;
    width: 100%;
	color: black;
  }

  #hud {
    display: flex;
    justify-content: space-between;
  }

  .hud-prefix {
    text-align: center;
    font-size: 2rem;
  }

  .hud-main-text {
    text-align: center;
    margin: 10px 0px 10px;
  }

  #hud-item {
    display: flex;
    text-align: center;
  }

  #game {
    padding: .5rem 2.25rem;
  }

  #question {
    font-size: 2rem;
    margin: 30px 0px 18px;
  }

  h1,
  h2,
  h3,
  h4 {
  }

  h1 {
    font-size: 1.5rem;
    color: #380df2;
  }

  h1 > span {
    font-size: 1.5rem;
    font-weight: 500;
  }

  h2 {
    font-size: 4.2rem;
    font-weight: 700;
  }

  h3 {
    font-size: 2.8rem;
    font-weight: 500;
  }

</style>

<script>
  // defining variables
  const question = document.getElementById('question');
  const choices = Array.from(document.getElementsByClassName('choice-text'));
  const progressText = document.getElementById('progressText');
  const scoreText = document.getElementById('score');
  const progressBarFull = document.getElementById('progressBarFull');
  const loader = document.getElementById('loader');
  const game = document.getElementById('game');
  const MAX_QUESTIONS = 3;
  const questionCounterText = document.getElementById('questionCounter');
  let currentQuestion = {};
  let acceptingAnswers = false;
  let score = 0;
  let questionCounter = 0;
  let availableQuestions = [];
  let questionTotal = 0

  let questions = [
    // Update MAX_QUESTIONS when adding more
    // all questions and choices
      {
          question: "Favorite color?",
          choice1: "blank",
          choice2: "blank",
          choice3: "purple",
          choice4: "blank",
          choiceAnswer: 3
      },
      {
          question: "Favorite game",
          choice1: "Apex",
          choice2: "blank",
          choice3: "blank",
          choice4: "blank",
          choiceAnswer: 1
      },
      {
          question: "Favorite place",
          choice1: "blank",
          choice2: "blank",
          choice3: "blank",
          choice4: "Greece",
          choiceAnswer: 4
      }
  ];

  startGame = () => {
    questionCounter = 0;
    score = 0;
    availableQuestions = [...questions];
    console.log(availableQuestions)
    getNewQuestion();
  }; 
  // plus minus which finds middle point score for each user
  endFunction = () => {
    if(userAnswer % 2 == 0) {
      let finalScore = userAnswer + .5
    }
    else {
      let finalScore = userAnswer - .5
    }
    localStorage.setItem("score", finalScore);
  }

   getNewQuestion = () => {
    // ends if no more questions
    if (availableQuestions.length === 0 || questionCounter >= MAX_QUESTIONS) {
      const resultContainer = document.getElementById("result");
      console.log(localStorage);
      console.log(localStorage.getItem("finalScore"));
      let matchScore = localStorage.getItem("finalScore")
      console.log(matchScore)
      // redirects window per score, matching system
      if (matchScore == 10.5) {
        return window.location.assign('/teamteam/dogs/dog_musa/'); 
      }

      localStorage.clear();
    }
    questionCounter++;
    questionCounterText.innerText = `Question: ${questionCounter}/${MAX_QUESTIONS}`;
    const questionIndex = Math.floor(Math.random() * availableQuestions.length);
    currentQuestion = availableQuestions[questionIndex];
    question.innerHTML = currentQuestion.question;

    choices.forEach((choice) => {
        const number = choice.dataset["number"];
        choice.innerHTML = currentQuestion["choice" + number];
    });
    // removes a question/ also determines when it ends
    availableQuestions.splice(questionIndex, 1);

    acceptingAnswers = true;
  };

  // this determines score for each choice, ex: choice3 = +3 for questionTotal
  choices.forEach((choice) => {
      choice.addEventListener('click', (e) => {
      
          if (!acceptingAnswers) return;

          acceptingAnswers = false;
          const selectedChoice = e.target;
          const selectedAnswer = selectedChoice.dataset['number'];
          const choiceAnswer = currentQuestion.choiceAnswer;
          console.log("Selected Answer: " + selectedAnswer);

          if (selectedAnswer == choiceAnswer)  {
            questionTotal = questionTotal + 1
            console.log("Score: " + questionTotal)
          }

          localStorage.setItem("finalScore", questionTotal)
          getNewQuestion(); 
    });
  });
  
  //starts game/quiz and will console the array of choices that the user has. IE 1-4
  startGame();
  console.log(choices)
  
</script>