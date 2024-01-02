<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Change Web Element Example</title>
</head>
<body>

  <p id="elementToChange">This is the initial text.</p>
  
  <!-- Placeholder text input for ID -->
  <input type="text" placeholder="Enter new ID" id="button">

  <!-- Placeholder text input for Name -->
  <input type="text" placeholder="Enter new Name" id="newNameInput">

  <!-- Button to change both ID and Name -->
  <button id="changeButton" onclick="changeElement()">Change Element</button>

  <script>
    // Function to be executed when the button is clicked
    function changeElement() {
      // Get the element by its ID
      var element = document.getElementById('elementToChange');
      
      // Get the input elements by their IDs
      var newIdInput = document.getElementById('button');
      var newNameInput = document.getElementById('newNameInput');

      // Array of predefined patterns for ID
      var idPatterns = ['greenbutton'];

      // Array of predefined patterns for Name
      var namePatterns = ['John', 'Jane', 'Doe'];

      // Get the current ID and Name of the input elements
      var currentId = newIdInput.id;
      var currentName = newNameInput.id;

      // Find the index of the current ID and Name in the arrays
      var currentIdIndex = idPatterns.indexOf(currentId);
      var currentNameIndex = namePatterns.indexOf(currentName);

      // Calculate the next indices (cycle back to the beginning if at the end)
      var nextIdIndex = (currentIdIndex + 1) % idPatterns.length;
      var nextNameIndex = (currentNameIndex + 1) % namePatterns.length;

      // Get the next ID and Name from the arrays
      var nextId = idPatterns[nextIdIndex];
      var nextName = namePatterns[nextNameIndex];

      // Change the ID and Name of the input elements
      newIdInput.id = nextId;
      newNameInput.id = nextName;

      // Clear the input values
      newIdInput.value = '';
      newNameInput.value = '';

      // Change the content of the element
      element.innerHTML = 'Element ID has been changed to: ' + nextId + ', and Name has been changed to: ' + nextName;
    }
  </script>

</body>
</html>
