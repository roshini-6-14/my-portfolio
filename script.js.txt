
const form = document.getElementById("recommendationForm");
const input = document.getElementById("recommendationText");
const list = document.getElementById("recommendationList");

function showPopup() {
  alert("Thank you! Your recommendation was submitted successfully.");
}

form.addEventListener("submit", function (event) {
  event.preventDefault();

  const message = input.value.trim();

  if (message.length === 0) {
    return;
  }

  const card = document.createElement("article");
  const paragraph = document.createElement("p");

  paragraph.textContent = message;
  card.appendChild(paragraph);

  list.appendChild(card);

  input.value = "";

  // Show popup only after a new recommendation is submitted.
  showPopup();
});
