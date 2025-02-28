<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>

    <style>
        body {
            background-image: url('https://images.unsplash.com/photo-1535350356005-fd52b3b524fb?fm=jpg&q=60&w=3000&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTh8fGRlc2lnbiUyMHdhbGxwYXBlcnxlbnwwfHwwfHx8MA%3D%3D');
            background-size: cover;
            background-repeat: no-repeat;
            background-position: center;
        }

        h1 {
            color: rgb(0, 0, 0);
            text-align: center;
        }

        h2 {
            color: rgb(0, 0, 0);
            text-align: center;
        }

        .centered-image {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .centered-form {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        .centered-paragraph {
            text-align: center;
            color: rgb(0, 0, 0);
        }

        .feedback-input {
            color: black; 
        }
    </style>
    <script>
        function showAlert(event) {
            event.preventDefault(); 
            var username = document.getElementById('fname').value;
            var password = document.getElementById('lname').value;
            alert('Username: ' + username +'\n'+'Password: ' + password);
        }

        function updateFeedbackColor() {
            var feedbackInput = document.getElementById('feedback');
            var feedbackValue = parseFloat(feedbackInput.value);
            if (feedbackValue < 0) {
                feedbackInput.style.color = 'red';
            } else if (feedbackValue > 0) {
                feedbackInput.style.color = 'blue';
            } else {
                feedbackInput.style.color = 'black';
            }
        }
    </script>
</head>
<body>
    <h1>Welcome to Login Page</h1>
    <h2>Login!</h2>
    <div class="centered-image">
        <img src="C:/Users/Onizea/Downloads/download-removebg-preview (2).png" alt="Login Image">
    </div>
    <div class="centered-form">
        <form action="/action_page.php" onsubmit="showAlert(event)">
            <label for="fname">Username:</label><br>
            <input type="text" id="fname" name="fname" value="amine" readonly><br>
            <label for="lname">Password:</label><br>
            <input type="text" id="lname" name="lname" value="*******"><br><br>
            <input type="submit" value="Login">
        </form>
        <p class="centered-paragraph">Don't have an account? <u><a href="register.html">register!</a></u></p>
        <input type="text" id="feedback" class="feedback-input" oninput="updateFeedbackColor()">
    </div>
</body>
</html>
