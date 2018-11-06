let readlineSync = require('readline-sync');

function getUserChoice(values) {
  userChoice = readlineSync.question('Choose: history, geography, entertainment, science, sports: ')
  userChoice = userchoice.toLowerCase();

  while(!values.includes(userChoice)) {
    console.log(`${userChoice} is not a valid answer, try again!`)
    userChoice = readlineSync.question('Choose: history, geography, entertainment, science, sports: ')
  }
  console.log(userChoice);
  return userChoice;
}

function game() {
  let choices = ['history', 'geography', 'entertainment', 'science', 'sports'];
  let points = 0;
  let userChoice;
  let continuePlaying = true;
  let wrongs = 0;
  let questions;
  let begin;
  let answer;
  let playAgain;

  while(continuePlaying === true) {
    userChoice = getUserChoice(choices);
    console.log(userChoice);
  }
}

funtion correct() {
  points += 200
  console.log(`You now have ${points}!`)
}

funtion wrongs() {
  wrongs ++
  if (wrongs >= 3) {
    console.log(`You lost. Game over.`)
    gameover();
  }
  else{
    console.log(`That's a strike! You now have ${wrongs}`)
  }
}

function winner() {
  if (points === 1000 && wrongs < 3) {
    console.log("You are a human encyclopedia! You got all right!")
  }
  else if (points === 600 && wrongs < 3) {
    console.log("You got most of the answers right, way to go!")
  }
  else if (points < 500 && wrongs < 3) {
    console.log("You didn't get enoguh correct answers. Better luck next time!")
  }
  else{
  }
}

function gameover() {
  console.log('Would you like to play again?')
  playAgain = readline-sync.question (`(Y)es | (N)o: `).toLowerCase()
  if (playAgain === "y" || playAgain === "yes") {
    newGame();
  }
  else {
    playAgain = false
  }
}

function newGame() {
  points = 0;
  wrongs = 0;
  playAgain = true;
}

while (playAgain == true) {
  points = 0;
  wrongs = 0;
}

// QUESTIONS

questions = [
  question1 = function () {
    console.log('In which year was America discovered?: ')
      answer = readline-sync.question('a.1942 | b.1492 | c.1294'),{
        trueValue: 'b || 1492'
        falseValue: ''
      });
      if (answer === true){
        correct()
      }else{
        wrong()
      }
  },

  question2 = function () {
    console.log('What is the capital of Spain?: ')
    asnwer = readline-sync.question('a.Barcelona | b.Sevilla | c.Madrid'),{
      trueValue: 'c || Madrid'
      falseValue: ''
    });
    if (answer === true){
      correct()
    }else{
      wrong()
    }
  },

  question3 = function () {
    console.log('Who was the voice behind Woody, the cowboy doll in Toy Story?: ')
    answer = readline-sync.question('a.Tom Hanks | b.Leonardo Di Caprio | c.The Rock'),{
      trueValue: 'a || Tom Hanks'
      falseValue: ''
    });
    if (answer === true){
      correct()
    }else{
      wrong()
    }
  },

  question4 = function () {
    console.log('How many time zones are there in the world?: ')
    answer = readline-sync.question('a.12 | b.18 | c.24'),{
      trueValue: 'c || 24'
      falseValue: ''
    });
    if (answer === true){
      correct()
    }else{
      wrong()
    }
  },

  question5 = function () {
    console.log('Who was the shortest player ever to play in the NBA?: ')
    answer = realine-sync.question('a.Tyrone Bogues | b.Earl Boykins | c.Greg Grant'),{
      trueValue: 'a || Tyrone Bogues'.toLowerCase()
      falseValue: ''
    });
    if (answer === true)
    correct()
  }else{
    wrong()
  }
},
]

//INTRODUCTION TO Game

console.log('Welcome to Express Trivia! Are you ready to prove you are as smart as you think?')
begin = readline-sync.question(` (Y)es | (N)o: `).toLowerCase()
if (begin === 'y' || begin === 'yes'){
} //not sure if this should go there

questions.forEach((question) => {
        if (wrongs < 3) {
          question()
        }
        else {
          console.log("Close, but not enough!Better luck next time!")
        }
      })
      winner()
    }
    else {
      break;
    }
  }
}


//everything after this is the alternative way I was using to create the questions and answers.
function getUserChoices(values) {
  userChoice = readlineSync.question('In which year was America discovered?: a.1942  b.1492  c.1294')
  userChoice = userchoice.toLowerCase();

  if (userChoice === 1492 || userChoice === b){
    console.log("Correct! You rock at history!");

  }else{
    console.log("Incorrect. Are you familiar with the term 'Encyclopedia'?")
  }
}

function getUserChoices(values) {
  userChoice = readlineSync.question('What is the capital of Spain?: a.Barcelona  b.Sevilla  c.Madrid')
  userChoice = userchoice.toLowerCase();

  if (userChoice === Madrid || userChoice === c) {
    console.log("Correct! You rock at geography too!");

  }else{
    console.log("Incorrect. You should know this, that's all I have to say")
  }
}

funtion getUserChoices(values) {
  userChoice = readlineSync.question('Who was the voice behind Woody, the cowboy doll in Toy Story?: a.Tom Hanks  b.Leonardo di Caprio  c.The Rock')
  userChoice = userchoice.toLowerCase();

  if (userChoice === Tom Hanks || userChoice === a) {
    console.log("Correct! You are on a roll!")

  }else{
    console.log("Incorrect. Do you really picture 'The Rock' as the voice behind a doll?")
  }
}

function getUserChoices(values) {
  userChoice = readlineSync.question('How many time zones are there in the world?: a.12  b.18  c.24')
  userChoice = userchoice.toLowerCase();

  if (userChoice === 24 || userChoice === c) {
    console.log("Correct! Impressive!")

  }else{
    console.log("Incorrect. This one was a tough one, you will get it next time!")
  }
}

function getUserChoices(values) {
  userchoice = readlineSync.question('Who was the shortest player ever to play in the NBA?: a.Tyrone Bogues  b.Earl Boykins  c.Greg Grant')
  userChoice = userchoice.toLowerCase();

if (userChoice === Tyrone Bogues || userChoice === a) {
  console.log("Correct! You did great!")

}else{
  console.log("Incorrect. They are all pretty short, but Bogues was the shortest of them all")
}

}

