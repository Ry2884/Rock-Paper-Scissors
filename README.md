# Rock-Paper-Scissors
My Rock, Paper Scissors Game

const getUserChoice = userInput => {
  userInput = userInput.toLowerCase();
  if (userInput === 'rock' || userInput === 'scissors' || userInput === 'paper' || userInput === 'bomb') {
    return userInput;
  } else {
    console.log('Error! Please type: rock, paper or scissors');
  }
}
const getComputerChoice = () => {
  const randomNumber = Math.floor(Math.random() * 3);
  switch (randomNumber) {
   case 0:
      return 'rock';
   case 1:
      return 'scissors';
   case 2:
      return 'paper';
}
}
const determineWinner = (userChoice, computerChoice) => {
  if (userChoice === computerChoice) {
    return 'It\'s a tie! Play again.';
}    
  if (userChoice === 'rock') {
    if (computerChoice === 'paper') {
      return 'Hal wins this round. Better luck next time!';
  } else {
     return 'You\'ve won!';
   } 
  }
  if (userChoice === 'bomb') {
    if (computerChoice === 'rock' || 'paper' || 'scissors'){
      return 'BOoooOOm goes the dynamite!';
  } else {
      return 'Hal wins this round. Better luck next time!';
  }
  }
  if (userChoice === 'paper') {
    if (computerChoice === 'scissors') {
      return 'Hal wins this round. Better luck next time!';
  } else {
      return 'You\'ve won!';
  }
}
  if (userChoice === 'scissors') {
    if (computerChoice === 'rock') {
      return 'Hal wins this round. Better luck next time!';
  } else {
      return 'You\'ve won!';
  }
  }
  if (userChoice === `${userInput}`) {
    return 'huh?';
   } else {
      return 'Hal wins this round. Better luck next time!'
   }
}
const playGame = () => {
  const userChoice = getUserChoice('donut');
  const computerChoice = getComputerChoice(); 
  console.log('You threw: ' + userChoice);
  console.log('The computer threw: ' + computerChoice)
  console.log(determineWinner(userChoice, computerChoice));
};

playGame()
