# common-problem-or-questions

How to convert form data to json 

const formElement = document.querySelector('form');

formElement.addEventListener('submit', (event) => {
  event.preventDefault(); // Stop page reload
  
  const formData = new FormData(formElement); // Gather inputs
  const jsonObject = Object.fromEntries(formData); // Convert to plain object
  const jsonString = JSON.stringify(jsonObject); // Convert to JSON string

  console.log(jsonString);
});
