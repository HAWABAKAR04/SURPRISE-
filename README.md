# SURPRISE-
!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SCOME Congratulations</title>
</head>
<body>
    <h1>Congratulations on Being a SCOME Member!</h1>
    <p>Please enter your name:</p>
    <input type="text" id="nameInput">
    <button onclick="showMessage()">Get Surprise</button>

    <div id="message" style="display: none;">
        <p id="congratsMessage"></p>
    </div>

    <script>
        function showMessage() {
            var name = document.getElementById("nameInput").value;
            var message = "Dear " + name + ",<br><br>Congratulations on being a valued member of SCOME. Your dedication and support are truly appreciated!<br><br>With warm regards,<br>HAWA, SCOME COORDINATOR";
            document.getElementById("congratsMessage").innerHTML = message;
            document.getElementById("message").style.display = "block";
        }
    </script>
</body>
</html>
