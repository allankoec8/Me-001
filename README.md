const noButton = document.getElementById('noButton');
const yesButton = document.getElementById('yesButton');
const response = document.getElementById('response');

let noCount = 0;
const messages = [
  "Are you sure?",
  "Really sure?",
  "Think again!",
  "Last chance!",
  "Do you mean yes? 😊",
  "You can't say no now!",
  "Just click yes already!",
  "Okay fine, I'll make it easy for you...",
  "YES or YES? 😉"
];

noButton.addEventListener('click', () => {
  noCount++;
  if (noCount < messages.length) {
    response.textContent = messages[noCount - 1];
  } else {
    response.textContent = "You have no choice but to say YES! 😘";
    noButton.style.display = "none";
    yesButton.textContent = "YES";
  }
});

yesButton.addEventListener('click', () => {
  response.textContent = "Yay! You made me the happiest person! ❤️";
  noButton.style.display = "none";
  yesButton.style.display = "none";
});
