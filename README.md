<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Change Web Element Example</title>
</head>
<body>

  <p id="elementToChange">This is the initial text.</p>

  <!-- Placeholder text input for entering a new name -->
  <input type="text" placeholder="Enter new name" id="maximus">

  <!-- Placeholder text input for entering a new email -->
  <input type="email" placeholder="Enter new email" id="murph">

  <!-- Button to change all IDs -->
  <button id="changeAllButton" onclick="changeAllIds()">Change All IDs</button>

  <script>
    // Function to be executed when the "Change All IDs" button is clicked
    function changeAllIds() {
      // Array of predefined patterns for all IDs
      var allPatterns = ['name', 'email'];

      // Iterate over all patterns and change the corresponding IDs
      allPatterns.forEach(function(pattern) {
        // Get the input element by its ID
        var inputElement = document.getElementById('enter' + pattern.charAt(0).toUpperCase() + pattern.slice(1) + 'Input');

        // Change the ID of the input
        inputElement.id = pattern + 'NewInput';
      });

      // Display a message indicating that all IDs have been changed
      alert('All input IDs have been changed.');
    }
  </script>

</body>
</html>
