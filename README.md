<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Change Web Element Example</title>
</head>
<body>

  <p id="elementToChange">This is the initial text.</p>
  <button id="changeButton">Change Element</button>

  <script>
    // Function to be executed when the button is clicked
    function changeElement() {
      // Get the element by its ID
      var element = document.getElementById('elementToChange');
      
      // Change the content of the element
      element.innerHTML = 'Element has been changed!';
    }

    // Get the button by its ID
    var changeButton = document.getElementById('changeButton');

    // Add a click event listener to the button
    changeButton.addEventListener('click', changeElement);
  </script>

</body>
</html>
