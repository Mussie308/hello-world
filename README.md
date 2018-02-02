function rockPaperScissors(userInput) {
var computerAnswers = [0, 0];
 for (var i = 0; i < 8; i++) {
    computerAnswers.push(Math.floor(Math.random() * 3));
    }
var answer = "";
switch(userInput) {
    case "Rock":
     answer = 0;
     break;
    case "Scissors":
     answer = 1;
     break;
    case "Paper":
     answer = 2;
     break;
   }
var scores = [];
var lossCount = 0;
var winCount = 0;
var tieCount = 0;
   for (var j = 0; j < 10; j++) {
     if (answer - computerAnswers[j] == 1 || answer - computerAnswers[j] == -2) {
       scores.push("loss");
       lossCount++;
     } else if (computerAnswers[j] - answer == 1 || computerAnswers[j] - answer == -2){
       scores.push("win");
       winCount++;
     } else if (answer == computerAnswers[j]) {
        scores.push("tie");
        tieCount++;
     }
}
if (userInput == "Scissors" || userInput == "Paper" || userInput == "Rock") {
  console.log("You have " + winCount + " wins, " + lossCount + " losses, and " + tieCount + " ties." );
} else {
    console.log("invalid input");
}
if (userInput == "Gun") {
    console.log("Your pitiful gun cannot hope to overcome the flurry of rock paper and scissors.");
}
}
