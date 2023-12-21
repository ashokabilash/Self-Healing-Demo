
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Change Web Element Example</title>
</head>
<body>

  <p id="elementToChange">This is the initial text.</p>
  <button id="changeButton" onclick="changeElement()">Change Element</button>

  <script>
    // Function to be executed when the button is clicked
    function changeElement() {
      // Get the element by its ID
      var element = document.getElementById('elementToChange');
      
      // Array of alternative IDs
      var alternativeIds = ['koney', 'uony', 'jony', 'lony'];

      // Get the current ID of the element
      var currentId = element.id;

      // Find the index of the current ID in the array
      var currentIndex = alternativeIds.indexOf(currentId);

      // Calculate the next index (cycle back to the beginning if at the end)
      var nextIndex = (currentIndex + 1) % alternativeIds.length;

      // Get the next ID from the array
      var nextId = alternativeIds[nextIndex];

      // Change the ID of the element
      element.id = nextId;

      // Change the content of the element
      element.innerHTML = 'Element ID has been changed to: ' + nextId;
    }
  </script>

</body>
</html>
