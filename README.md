# Javascript projects

//Kelvin Weather Calculation
const Kelvin = 50; // Kelvin will always equal 293
const Celsius = Kelvin-273; // celsius will always be 273 less than Kelvin
let Fahrenheit = Celsius*(9/5)+32; // calculating fahrenheit from celsius
Fahrenheit = Math.floor(Fahrenheit); // puts Fahrenheit as whole number
let Newton = Celsius * (33/100); // convert Celsius to Newton
Newton = Math.floor(Newton);
console.log(`The temperature is ${Fahrenheit} degrees Fahrenheit.`);
console.log(`The temperature is ${Newton} degrees Newton`);

//Calculate dog years
//Stating my age
const myAge = 29;
let earlyYears = 2;
earlyYears = earlyYears * 10.5;
let laterYears = myAge - 2;
laterYears *= 4;
const myAgeInDogYears = earlyYears + laterYears;
const myName = 'Taylor Majewski';
'Taylor Majewski'.toLowerCase();
console.log(`My name is ${myName}. I am ${myAge} years old in human years which is ${myAgeInDogYears} years old in dog years`);

//Magic Eight Ball
let userName = "";
userName ? console.log("Hello, ${userName}!") : console.log("Hello!");
const userQuestion = "Will I pass this exam?";
console.log("Will I pass this exam?");

let randomNumber = Math.floor(Math.random() * 8);
let eightBall = '' 

switch (randomNumber) {
  case 0 :
    console.log('It is certain');
  break;
  case 1 :
    console.log('It is decidedly so');
  break;

  case 2 :
    console.log('Reply hazy try again');
  break;

  case 3 :
    console.log('Cannot predict now');
  break;

  case 4 :
    console.log('Do not count on it');
  break;

  case 5 :
    console.log('My sources say no');
  break;

  case 6 :
    console.log('Outlook not so good');
  break;

  case 7 :
    console.log('Signs point to yes');
  break; }

//Race Day
let raceNumber = Math.floor(Math.random() * 1000);
let registeredEarly = false;
let runnerAge = 18;

if(registeredEarly && runnerAge > 18) {
  raceNumber += 1000
};

if(runnerAge > 18 && registeredEarly) { 
  console.log(`Runner ${raceNumber}, your race start time is 9:30am.`);
}
else if(!registeredEarly && runnerAge > 18) {
  (console.log(`Runner ${raceNumber}, your race start time is 11:00am.`));
  }
else if(runnerAge < 18) 
  console.log(`Runner ${raceNumber}, your race start time is 12:30pm.`);

else(console.log('See registration desk.'));

//rock, paper, scissors
const getUserChoice = (userInput) => {
  userInput = userInput.toLowerCase();
  if (userInput === 'rock' || userInput === 'scissors' || userInput === 'paper' || userInput === 'bomb') {
    return userInput;
  }
    else {
      console.log('Invalid Entry');
    }
}

const getComputerChoice = () => {
  const randomNumber = Math.floor(Math.random() * 3)
  switch (randomNumber) {
    case 0: 
      return 'rock';
    case 1: 
      return 'paper';
    case 2: 
      return 'scissors';
  }
};


const determineWinner = (userChoice, computerChoice) => {
  if (userChoice === computerChoice) {
    return 'The game is a tie.';
  }
  if (userChoice === 'bomb') {
    return 'You blew up the computer!';
  }
  if (userChoice === 'rock') {
    if (computerChoice === 'paper') {
      return "The computer won.";}
      else {
        return "You beat the computer!";
    }
  }
  if (userChoice === 'paper') {
    if (computerChoice === 'scissors') {
      return "The computer won."}
      else { 
        return "You beat the computer!";
      }
    }
  if (userChoice === 'scissors') {
    if (computerChoice === 'rock') {
      return "The computer won."}
      else {
        return "You beat the computer!";
      }
      }
    };

 const playGame = () => {
   const userChoice = getUserChoice('bomb');
   const computerChoice = getComputerChoice();
   console.log('You threw: ' + userChoice);
   console.log('The computer threw ' + computerChoice);

   console.log(determineWinner(userChoice, computerChoice));
 };

 playGame()
 
 //Sleep Debt Calculator
 const getSleepHours = day => {
  
  switch(day) {
    case "Monday":
      return 8
      break;
    case "Tuesday": 
      return 5
      break;
    case "Wednesday":
      return 9
      break;
    case "Thursday":
      return 3
      break;
    case "Friday": 
      return 11
      break;
    case "Saturday":
      return 6
      break;
    case "Sunday":
      return 8
      break;

    default: 
      return "Error!"
  }
};
const getActualSleepHours = () => getSleepHours('Monday') + getSleepHours('Tuesday') + getSleepHours('Wednesday') + getSleepHours('Thursday') + getSleepHours('Friday') + getSleepHours('Saturday') + getSleepHours('Sunday');

const getIdealSleepHours = () => {
 let idealSleepHours = 8;
  return idealSleepHours * 7;
};

const calculateSleepDebt = () => {
  const actualSleepHours = getActualSleepHours();
  const idealSleepHours = getIdealSleepHours ();


if (actualSleepHours === idealSleepHours) {
  console.log('You are getting the perfect amount of sleep.')
} else if (actualSleepHours > idealSleepHours) {
  console.log('You are getting too much sleep.')
} else {
  console.log('You are not getting enough sleep.')
}
};
calculateSleepDebt();
