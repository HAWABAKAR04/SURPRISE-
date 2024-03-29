<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TODAY'S GIFT</title> <!-- Updated title -->
    <style>
        /* CSS styling for the virtual gift package */
        body {
            background-image: url('medical-education-background.jpg'); /* Background image representing medical education */
            background-size: cover;
            font-family: Arial, sans-serif;
            text-align: center;
            color: white; /* Text color to contrast with the background */
        }
        .gift-box {
            width: 150px;
            height: 150px;
            background-image: url('gift-box.png'); /* Gift box image */
            background-size: cover;
            display: inline-block;
            margin: 20px;
            cursor: pointer;
        }
        .gift-box:hover {
            animation: bounce 0.5s ease-in-out infinite; /* Add a bouncing animation on hover */
        }
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
    </style>
</head>
<body>
    <h1 id="title"></h1> <!-- Updated name of the gift box channel -->
    <div class="gift-box" onclick="revealMessage(this)"></div> <!-- Gift box element with onclick event -->

    <!-- JavaScript to reveal a congratulatory message when clicking on the gift box -->
    <script>
        function revealMessage(box) {
            // Add animation or transition to simulate opening the gift box
            box.style.transform = "rotateY(180deg)";
            
            // Display a typing effect for the congratulatory message
            var message = "🎉 Hooray! Congratulations to our incredible SCOME members! 🌟 Your unwavering support and enthusiasm have brought so much joy and success to our team! 🥳 Let's celebrate together! 🎈";
            var title = "TODAY'S GIFT";
            var speed = 50; // Adjust the speed of typing
            
            document.getElementById("title").innerText = ""; // Clear the title initially
            
            // Typing effect for the title
            for (var i = 0; i < title.length; i++) {
                setTimeout(function() {
                    document.getElementById("title").innerText += title.charAt(i);
                }, speed * i);
            }
            
            // Typing effect for the message
            setTimeout(function() {
                box.innerHTML = ""; // Clear the box initially
                for (var i = 0; i < message.length; i++) {
                    setTimeout(function() {
                        box.innerHTML += message.charAt(i);
                    }, speed * i);
                }
            }, speed * title.length);
        }
    </script>
</body>
</html>
