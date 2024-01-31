
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hotel Booking</title>
  <style>
    .Change-Web-Element-Example {
      display: none;
    }
    body {
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      background: url('your-hotel-background-image.jpg') center/cover no-repeat; /* Add your background image URL */
      filter: brightness(90%); /* Apply a slight blue tint to the background */
    }

    header {
      text-align: center;
      margin-bottom: 10px;
    }

    h1 {
      font-size: 36px;
      margin: 0;
      font-weight: bold;
      color: #000; /* Bold black heading color for better visibility on the background */
      font-family: 'Arial Black', sans-serif; /* Bold font style for the heading */
    }

    h2 {
      font-size: 16px;
      margin: 0;
      color: #ddd; /* Light gray color for subheading */
    }

    .login-container {
      background-color: rgba(255, 255, 255, 0.8); /* Semi-transparent white background */
      border-radius: 8px;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.2); /* Box shadow for the form */
      overflow: hidden;
      width: 400px;
      transform: translateY(0);
      transition: transform 0.5s ease-in-out;
    }

    .login-container:hover {
      transform: translateY(-10px); /* Add a subtle upward lift on hover */
    }

    form {
      padding: 20px;
      transition: transform 0.5s ease-in-out;
    }

    form.active {
      transform: translateX(-100%);
    }

    label {
      display: block;
      margin-bottom: 8px;
      color: #333;
      font-weight: bold; /* Bold font for labels */
    }

    input, select, textarea {
      width: 100%;
      padding: 8px;
      margin-bottom: 16px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
      transition: border-color 0.3s ease-in-out;
      font-weight: bold; /* Bold font for input elements */
    }

    input:focus, select:focus, textarea:focus {
      border-color: #3498db;
    }

    .required-info {
      display: flex;
      align-items: center;
      color: #777;
      margin-bottom: 16px;
      font-weight: bold; /* Bold font for the info text */
    }

    .info-icon {
      margin-right: 8px;
      color: #f00;
    }

    .submit-button {
      background-color: #3498db; /* Button color */
      color: #fff; /* Button text color */
      padding: 10px 20px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      transition: background-color 0.3s ease-in-out;
      margin-right: 10px; /* Add margin for spacing between buttons */
      font-weight: bold; /* Bold font for buttons */
    }

    .submit-button:hover {
      background-color: #2980b9; /* Button color on hover */
    }

    .celebration-message {
      display: none;
      text-align: center;
      margin: 30px;
      color: #4CAF50; /* Green color for celebration message */
      font-size: 24px;
      font-weight: bold;
    }

    .celebration-animation {
      animation: bounce 1s infinite; /* Add a bounce animation */
    }

    @keyframes bounce {
      0%, 20%, 50%, 80%, 100% {
        transform: translateY(0);
      }
      40% {
        transform: translateY(-20px);
      }
      60% {
        transform: translateY(-10px);
      }
    }
  </style>
</head>
<body>
  <header>
    <h1 style="color: rgb(7, 152, 248); text-shadow: 1px 1px 1px rgba(255, 255, 255, 0.5);">Hotel Booking</h1>
</header>

  <div class="login-container">
    <form id="hotelLoginForm">
      <label for="name">Name:</label>
      <div>

        <input type="date" id="poiu" name="departureDate" required>
        
        



      </div>
      

      <label for="email">E-mail:</label>
      
      <div class="required-info">
        <span class="info-icon">ℹ️</span>
        This field is required.
      </div>

      <label for="roomType">Room Type:</label>
      <select id="roomType" name="roomType" required>
        <option value="single">Single</option>
        <option value="double">Double</option>
        <option value="suite">Suite</option>
      </select>

      <label for="arrivalDate">Arrival Date:</label>

      <label for="departureDate">Departure Date:</label>
      <div>
        <input type="date" id="asdf" name="arrivalDate" required>

      </div>
      <div>
        <input type="email" id="zxcv" name="email" required>
        
      </div>
      

      <label for="specialRequests">Special Requests:</label>
      <textarea id="specialRequests" name="specialRequests" rows="4"></textarea>
      <div>
        <input type="text" id="qwer" name="name" required>
        
      </div>

      <button type="submit" class="submit-button">Submit</button>
    </form>

    <div id="celebrationMessage" class="celebration-message">
      Thanks for submitting! 🎉
    </div>
  </div>

  <script>
    const form = document.getElementById('hotelLoginForm');
    const celebrationMessage = document.getElementById('celebrationMessage');

    form.addEventListener('submit', function (e) {
      e.preventDefault();
      form.classList.add('active');
      showCelebrationMessage();
    });

    function showCelebrationMessage() {
      // Hide the form
      form.style.display = 'none';

      // Show the celebration message
      celebrationMessage.style.display = 'block';
      celebrationMessage.classList.add('celebration-animation');
    }
  </script>
</body>
</html>
